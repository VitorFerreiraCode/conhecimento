
---

### Definindo um componente:

1. **@Component *decorator***
	- Contém o *metadata* do componente: *selector, template url, providers, etc*.
2. **Template HTML**
	- Define como aquele componente será renderizado no DOM, pode ser *inline* ou num arquivo externo.
3. **Selector**
	- É o nome do (*seletor CSS*) que você usa no HTML para "injetar" o componente.
4. **Classe TypeScript**
	- Implementa a lógica do componente: interage com o usuário, injeta serviços, responde a eventos, trata dados, etc.


**user-profile.ts**

```
@Component({ 
	selector: 'user-profile', 
	template: ` 
		<h1>User profile</h1> 
		<p>This is the user profile page</p> 
	`,
	styles: `h1 { font-size: 3em; }`
})

export class UserProfile { /* O Código do seu componente vai aqui */ }
```

### Separando HTML e CSS em arquivos separados

**user-profile.ts**
```
@Component({ 
	selector: 'user-profile', 
	templateUrl: 'user-profile.html', 
	styleUrl: 'user-profile.css',
})

export class UserProfile { /* O comportamento do componente é definido aqui */}
```

**user-profile.html**
```
<h1>Use profile</h1>
<p>This is the user profile page</p>
```

**user-profile.css
```
h1 { font-size: 3em;}
```

### Usando Componentes

![[Components-user]]


### Importar e Usar Componentes

1. Adicione um **import** do componente que você quer usar no seu arquivo TypeScript.
2. No seu **@Component *decorator*** importe de fato o componente que quer usar.
3. No seu template de componente, adicione um elemento de seleção do componente que quer usar.

**user-profile.ts**
```
@Component({ 
	selector: 'user-profile',
	imports: [ProfilePhoto],
	template: ` 
		<h1>User profile</h1> 
		<profile-photo />
		<p>This is the user profile page</p> 
	`,
})

export class UserProfile { 
/* O Código do seu componente vai aqui */ 
}
```
