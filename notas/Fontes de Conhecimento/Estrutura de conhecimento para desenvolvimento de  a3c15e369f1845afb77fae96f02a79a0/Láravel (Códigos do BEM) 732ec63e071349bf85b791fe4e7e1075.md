# Láravel (Códigos do BEM)

# Dicas Iniciais

[Apesentação](La%CC%81ravel%20(Co%CC%81digos%20do%20BEM)%20732ec63e071349bf85b791fe4e7e1075/Apesentac%CC%A7a%CC%83o%2068e549e2412541fd8f72dfdd2f630191.md)

[Instalação aprendizagem 1](La%CC%81ravel%20(Co%CC%81digos%20do%20BEM)%20732ec63e071349bf85b791fe4e7e1075/Instalac%CC%A7a%CC%83o%20aprendizagem%201%203b256e0b0b2b48e59bbea0a6e09e1996.md)

[Instalação aprendizagem 2](La%CC%81ravel%20(Co%CC%81digos%20do%20BEM)%20732ec63e071349bf85b791fe4e7e1075/Instalac%CC%A7a%CC%83o%20aprendizagem%202%20124489d81ea64845a7ae558c108e784e.md)

# Aulas

[Aula 02](La%CC%81ravel%20(Co%CC%81digos%20do%20BEM)%20732ec63e071349bf85b791fe4e7e1075/Aula%2002%20b73dce446ab647d89aa60451a48cd290.md)

[Aula 03](La%CC%81ravel%20(Co%CC%81digos%20do%20BEM)%20732ec63e071349bf85b791fe4e7e1075/Aula%2003%204d2173645a9146bc8b3d800bad19e077.md)

[Aula 04](La%CC%81ravel%20(Co%CC%81digos%20do%20BEM)%20732ec63e071349bf85b791fe4e7e1075/Aula%2004%2041ce4f4f5ce0463a94cd5c74fe6fe0f7.md)

[Aula 05](La%CC%81ravel%20(Co%CC%81digos%20do%20BEM)%20732ec63e071349bf85b791fe4e7e1075/Aula%2005%20cd50cb615ad24960840ee0252a9c0c60.md)

[Aula 06](La%CC%81ravel%20(Co%CC%81digos%20do%20BEM)%20732ec63e071349bf85b791fe4e7e1075/Aula%2006%20cd0891d5fdbc476b8023c3bf6ed5fcc3.md)

[Aula 07](La%CC%81ravel%20(Co%CC%81digos%20do%20BEM)%20732ec63e071349bf85b791fe4e7e1075/Aula%2007%20fbe0b4366ff0450fbd6828cf1c89d09a.md)

[Aula 08](La%CC%81ravel%20(Co%CC%81digos%20do%20BEM)%20732ec63e071349bf85b791fe4e7e1075/Aula%2008%20134fc7d64ff74261ac8e8b2a2e7410b2.md)

# Anotações a parte

Alteração de tabela e inserção de valor

![Untitled](La%CC%81ravel%20(Co%CC%81digos%20do%20BEM)%20732ec63e071349bf85b791fe4e7e1075/Untitled.png)

![Untitled](La%CC%81ravel%20(Co%CC%81digos%20do%20BEM)%20732ec63e071349bf85b791fe4e7e1075/Untitled%201.png)

Insersão de dados do request no banco

```php
$variavel = Model::create($request->all());
```

Validation

```php
public function update(Request $request)
{
	$validated = $request->validate([
		'email' => 'required|email|unique:users',
		'password' => Password::required()->min(8)->uncompromised(),
	]);
	$request->user()->update($validated);

}
```