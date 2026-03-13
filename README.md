# Prime Residence — Landing Page Imobiliária

> Landing page premium para imobiliária de alto padrão, construída com **Angular 17** (Standalone Components) + **Tailwind CSS 3**.

---

## 🚀 Como Rodar

### Pré-requisitos
- Node.js 18+
- npm 9+
- Angular CLI 17+

### Instalação

```bash
# 1. Clone ou extraia o projeto
cd prime-residence

# 2. Instale as dependências
npm install

# 3. Instale o Angular CLI globalmente (se ainda não tiver)
npm install -g @angular/cli@17

# 4. Inicie o servidor de desenvolvimento
ng serve

# 5. Acesse no navegador
# http://localhost:4200
```

### Build para Produção

```bash
ng build --configuration production
# Os arquivos ficam em /dist/prime-residence/
```

---

## 📁 Estrutura de Pastas

```
prime-residence/
├── src/
│   ├── app/
│   │   ├── components/
│   │   │   ├── navbar/
│   │   │   │   └── navbar.component.ts        # Navbar fixa com menu mobile
│   │   │   ├── hero/
│   │   │   │   └── hero.component.ts          # Hero com barra de busca
│   │   │   ├── featured-properties/
│   │   │   │   └── featured-properties.component.ts  # Cards de imóveis
│   │   │   ├── why-choose-us/
│   │   │   │   └── why-choose-us.component.ts  # Diferenciais
│   │   │   ├── about/
│   │   │   │   └── about.component.ts         # Sobre a imobiliária
│   │   │   ├── stats/
│   │   │   │   └── stats.component.ts         # Estatísticas/números
│   │   │   ├── testimonials/
│   │   │   │   └── testimonials.component.ts  # Depoimentos
│   │   │   ├── cta-banner/
│   │   │   │   └── cta-banner.component.ts    # CTA intermediário
│   │   │   ├── lead-form/
│   │   │   │   └── lead-form.component.ts     # Formulário com validação
│   │   │   └── footer/
│   │   │       └── footer.component.ts        # Rodapé completo
│   │   ├── data/
│   │   │   └── mock-data.ts                   # Dados mockados (imóveis, depoimentos, etc.)
│   │   ├── models/
│   │   │   └── property.model.ts              # Interfaces TypeScript
│   │   └── app.component.ts                   # Componente raiz
│   ├── styles.css                             # Estilos globais + Tailwind
│   ├── index.html                             # HTML base
│   └── main.ts                                # Bootstrap Angular
├── tailwind.config.js                         # Configuração Tailwind (fontes, cores custom)
├── postcss.config.js
├── angular.json
├── tsconfig.json
├── tsconfig.app.json
└── package.json
```

---

## 🧩 Componentes

| Componente | Seção | Funcionalidade |
|---|---|---|
| `NavbarComponent` | Header | Navbar fixa com scroll detection e menu mobile |
| `HeroComponent` | Hero | Headline + barra de busca com filtros |
| `FeaturedPropertiesComponent` | Imóveis | Grid de cards com filtros por tipo |
| `WhyChooseUsComponent` | Diferenciais | 4 cards de diferenciais |
| `AboutComponent` | Sobre | Texto institucional + imagem |
| `StatsComponent` | Números | Estatísticas da empresa |
| `TestimonialsComponent` | Depoimentos | 3 depoimentos com estrelas |
| `CtaBannerComponent` | CTA | Banner de conversão |
| `LeadFormComponent` | Formulário | Form reativo com validação Angular |
| `FooterComponent` | Rodapé | Footer completo |

---

## 🎨 Design System

### Paleta de Cores

| Cor | Uso |
|---|---|
| `gold-500` (#d49a10) | Cor de destaque principal |
| `charcoal-950` (#1a1a1a) | Fundo escuro, textos principais |
| `charcoal-50` | Fundos suaves |
| `navy-950` | Overlays escuros |
| `white` | Fundos limpos |

### Fontes

- **Display**: Cormorant Garamond (títulos elegantes, serifada)
- **Body**: DM Sans (corpo do texto, leiturabilidade)

### Classes Utilitárias Customizadas (styles.css)

```css
.btn-gold          /* Botão primário dourado */
.btn-outline-gold  /* Botão outline dourado */
.btn-dark          /* Botão preto */
.section-label     /* Rótulo dourado acima dos títulos */
.section-title     /* Título principal de seção */
.gold-line         /* Linha decorativa dourada */
.input-field       /* Campo de formulário padrão */
.property-card     /* Card de imóvel com hover */
```

---

## 🔧 Integração com API

Os dados estão mockados em `src/app/data/mock-data.ts`. Para integrar com uma API real:

```typescript
// Exemplo: criar um service
// src/app/services/property.service.ts

@Injectable({ providedIn: 'root' })
export class PropertyService {
  private apiUrl = 'https://sua-api.com/api';

  constructor(private http: HttpClient) {}

  getProperties(): Observable<Property[]> {
    return this.http.get<Property[]>(`${this.apiUrl}/properties`);
  }

  getFeatured(): Observable<Property[]> {
    return this.http.get<Property[]>(`${this.apiUrl}/properties/featured`);
  }
}
```

---

## ✅ Features Implementadas

- [x] Navbar fixa com scroll detection
- [x] Menu hamburger mobile com animação
- [x] Hero com barra de busca (tipo, localização, preço)
- [x] Grid de imóveis com filtro por tipo
- [x] Cards com badges (Novo, Destaque, Luxo, Exclusivo)
- [x] Hover states refinados nos cards
- [x] Seção de diferenciais (fundo escuro)
- [x] Seção "Sobre" com imagens sobrepostas
- [x] Seção de estatísticas (fundo dourado)
- [x] Depoimentos com estrelas e avaliação geral
- [x] CTA banner com imagem de fundo
- [x] Formulário reativo com validação Angular
- [x] Feedback visual de sucesso no envio
- [x] Footer completo com redes sociais
- [x] Responsivo mobile-first
- [x] Animações CSS (fade-in-up)
- [x] Scroll suave entre seções
- [x] Fontes premium (Google Fonts)
- [x] Standalone Components (Angular 17+)
- [x] Signals (reatividade moderna do Angular)
- [x] TypeScript com interfaces tipadas

---

## 📞 Dados de Contato (Mock)

Atualize em `footer.component.ts` e `lead-form.component.ts`:
- Telefone: `(11) 99999-9999`
- E-mail: `contato@primeresidence.com.br`
- Endereço: `Av. Brigadeiro Faria Lima, 2000 — Jardins, SP`
- CRECI: `J-12345`
