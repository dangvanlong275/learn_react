## Hook useState

### Khi nào sẽ sử dụng
    Khi muốn dữ liệu người dùng thay đổi thì giao diện tự động thay đổi (render lại dữ liệu)

### Lưu ý
- Component sẽ được render lại khi setState 
- Giá trị initState chỉ dùng cho lần đầu khởi chạy

## useEffect
 - Cả 3 trường hợp đều được gọi khi component được mounted lần đầu
 - Cleanup function luôn được gọi trước khi component unmounted
 - Cleanup function luôn được gọi trước khi callback được gọi (trừ mounted)
## userEffect(callback)
- Gọi callback mỗi khi component re-render
- Gọi callback sau khi component thêm element vào DOM
## userEffect(callback, [])
- Chỉ gọi callback một lần duy nhất khi component được mounted
## userEffect(callback, [deps])
- Callback được gọi mỗi khi deps thay đổi giá trị với toán tử ===
## useRef
- Chỉ sử dụng giá trị đầu tiên khi component được tạo 
image.png

## React.memo HOC
- Là hight order component
- Check các props được truyền vào component có bị thay đổi hay không để re-render lại component
image.png

## useCallback Hook
- Trả về tham chiếu của callback và cách sử dụng tương tự useEffect
image.png
- Kết hợp giữa memo và useCallback nếu không có memo thì không cần phải sử dụng

## useMemo

- Tránh phải thực hiện một logic nào đó không cần thiết

## userReducer
1. InitState
2. Actions
3. Reducer
4. Dispatch

![](https://lh3.googleusercontent.com/pw/AMWts8Dd0Vh5KjX-6B1xX0pngi9hP4OOciUoLGBqhN2-dlPlBEdQzry0t28H9MSx6pfhRxlv7sOxbLFM5H-jgC_uoNYsqmPzBn1QAfEQKWhBXaJwLeEcawiC0YRGIU9eWUEYpXPp1At7Ft-oBzKtc9jmJ5k9=w570-h537-s-no?authuser=0)

- Handle reducer giống như redux

![](https://lh3.googleusercontent.com/pw/AMWts8D9YANULygg8uwAEpHmtvxROQOaX8J7y44Gj868KunM8CikbGQ_8Rnh7cifucl8CH8MTkwlsGvlWmYlF5iZKiyTO8dFbfV4DJwZbXVnpyGgV0GtntXxCfF3T5GBb3gGCpGv6_TsyEHLtrZHTn-ug0w5=w556-h436-s-no)

## useContext
- Giúp đơn giản hóa việc truyển dữ liệu từ component cha sang component con mà không cần tới props

 - Sử dụng tại component cha
 - export const ThemeContext = createContext()

 ![](https://lh3.googleusercontent.com/pw/AMWts8DITuslYVpUzFWBRVmVJlrsv_BmR-FoD_j4of9veYA0ZZ2aGNSgwy2SOy28ED-IXOlzoSn4yOgqvYZA98oJETHdh0Os2EF7HCjA28kVdrXEZ2ycaoWj5vzJuE21BFLj-8XDCI90xyQP-zgkrtzq7IeH=w553-h494-s-no?authuser=0)

 - Sử dụng tại component con

 ![](https://lh3.googleusercontent.com/pw/AMWts8DkhuR7d2SIUwE7sy2BKoAi4KQc3VQv51IXnN0KoOtVUtDsOQu302Dz7QMlzy4arrC6C5rdrRte2YBY0rEPkMRim8OKAaSltJ5hsRhtUYt6tRLFHinZgNEdAd4pY-NaHrXO0mFaY2qLgxGvEPKRm-SO=w550-h421-s-no?authuser=0)

 ## useContent + useReducer
 [github](https://github.com/OrigamiTobichi/use-context-reducer)

 ## useImperativeHandle hook
 - Giúp tùy chỉnh được Ref của một function component

 ![](https://lh3.googleusercontent.com/pw/AMWts8DDxqHSDv6-SsCNXeeLJgw_IHmQ8GE9BSD1f-ZpcwWtHLeVlGsvaXKXOgtkw4cGucN-MjMCJuSJKjdEOe1Ix92LrhMn9QUVqjV7SUpxvW-Y3TxEgP2OkMG6vo68uD31t7fAZfwgVqMFwgv-JPshDeQZ=w604-h526-s-no?authuser=0)
 ![](https://lh3.googleusercontent.com/pw/AMWts8CPHQbL5I_QtP17Ef_1XGrUfi4qi-e84Buvhdqu4XhzQ9m5Fl3lmV4Zh90jQQprvfNWaBegjoyDtY5n8sLBQBb8MPEqp-45Fv-UQVzj86sX8upQdS2jn0umKz-xahmxM--N_LqXjtjsRpDkk_OjiMr-=w580-h523-s-no?authuser=0)
