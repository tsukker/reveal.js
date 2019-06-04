# タイトル Title

~~{:main}~~
name, etc

---

## Slide 1

.lead sentence

Notes:
speaker notes

---

## Slide 2-1

. vertical slide ↓

>>>

## Slide 2-2

. vertical slide ↑

---

## Edit!

. example: next page→

---

### HOCよりもRender Props

.react-routerのmjackson氏が推奨<br>
データの流入元が明示的


~~{:main}~~      

##### コンポーネント定義例
```javascript
const ParentComponent extends Component {
    constructor() {
        this.state = { value: 1 };
    }
    render () {
        return (<div> {props.render(this.state)} </div>);
    }
)

const ChildComponent = (props) => (
    <ParentComponent render={ (value)=> { <button>{value}</button> } />);
```
~~x~~

~~{:footer}~~    
HOC: Higher Order Componentの略
~~x~~

---

### オニオンアーキテクチャ

.Jeffrey Palermo氏が提唱したアーキテクチャ
<br>外側の層から内側の層のみ依存関係

~~{:left}~~

.特徴 :mag:
 - ドメインモデルは完全独立
   * インフラの寿命は３年
 - 依存性逆転の法則(DIP)
   * 内: インタフェースを定義
   * 外: 具象を実装
~~x~~

~~{:right}~~
![arch{90%,80%}](https://camo.qiitausercontent.com/53096c6054e84aed4e84277b5302f60fd62ec115/68747470733a2f2f71696974612d696d6167652d73746f72652e73332e616d617a6f6e6177732e636f6d2f302f3136303435312f62393238356663372d343235642d313939392d386332392d3437323664666264646139302e706e67)
~~x~~

~~{:footer}~~
 画像出典: [ドメイン駆動 + オニオンアーキテクチャ概略](https://qiita.com/little_hand_s/items/2040fba15d90b93fc124)
~~x~~
