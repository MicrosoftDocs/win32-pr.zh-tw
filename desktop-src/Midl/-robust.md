---
title: /robust 參數
description: /Robust 參數會告知 MIDL 編譯器產生額外的錯誤檢查資訊，而 NDR 引擎會使用此資訊在執行時間執行完整性檢查。
ms.assetid: 7a858600-ea06-4396-9a1b-240d646e8c7d
keywords:
- /robust 參數 MIDL
topic_type:
- apiref
api_name:
- /robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974f9530006c03a041d9d444c41f9c5ca01569c0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841123"
---
# <a name="robust-switch"></a>/robust 參數

**/Robust** 參數會告知 MIDL 編譯器產生額外的錯誤檢查資訊，而 NDR 引擎會使用此資訊在執行時間執行完整性檢查。

``` syntax
midl /robust {/Oicf | /Oif }
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*/Oicf* 
</dt> <dd></dd> <dt>

*/Oif* 
</dt> <dd>

這些參數在其功能上都相同。 他們會指定封送處理的無程式碼 proxy 方法，並使用快速格式字串來改善效能。 請參閱/ [**Oi**](-oi.md)。

</dd> </dl>

## <a name="remarks"></a>備註

使用 **/robust** 參數會產生額外的資訊，以允許 (NDR) 引擎的網路資料表示，在動態陣列、等位和 DCOM 應用程式的 [**輸出**](out-idl.md) 介面指標中，對相互關聯的引數執行執行階段錯誤檢查。 **/Robust** 參數僅適用于 windows 2000 和更新版本的 Windows。

相互關聯的引數是使用任何屬性的引數，這些屬性可在執行時間決定資料物件的大小： [**大小 \_ 為**](size-is.md)、 [**長度 \_ 為**](length-is.md)、 [**第一個 \_ 為**](first-is.md)、 [**最後一個 \_**](last-is.md)、 [**最大 \_**](max-is.md)值、 [**參數 \_ 為**](switch-is.md)，而且 [**iid \_ 為**](iid-is.md)。 根據網路標記法的憑證-DCE 規格，此相互關聯的引數會出現在兩個不同的位置。 例如，請考慮使用 **大小 \_ 為** 屬性的一般用法：

``` syntax
HRESULT Func1([in] long Size, 
              [in, size_is(Size)]BAR_TYPE *pBarType);
```

在此範例中，用戶端會傳遞 long，以指定橫條圖類型區塊的大小 \_ (以) 的橫條類型元素數目為單位 \_ ，並以指標指向橫條圖類型的實際區塊 \_ 。 Size 引數與 pBarType 引數相互關聯。 根據憑證-DCE 規格，Size 引數會在網路上以兩次表示（先做為本身，然後使用 \_ 代表 pBarType 引數的橫條類型元素陣列）。 每個引數會根據其本身的線路表示來獨立進行封送。 一般來說，大小引數及其複製（用來代表另一個引數的一部分）具有相同的值。 但是，如果大小引數損毀 (例如，當橫條類型的區塊大於配置) 的區塊時， \_ 伺服器應用程式可能會停止回應，因為它會使用 Size 引數的值來測量傳入的資料。

需要 **/robust** 參數才能使用 [**range**](range.md) 屬性來執行有效的範圍檢查。

## <a name="examples"></a>範例

**midl/robust/Oicf filename .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Oi**](-oi.md)
</dt> <dt>

[**範圍**](range.md)
</dt> </dl>

 

 




