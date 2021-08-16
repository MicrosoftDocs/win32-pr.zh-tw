---
title: 類別圖示
description: 用來代表類別物件的圖示可以在 DisplaySpecifiers 容器的 >iconpath 屬性中指定。
ms.assetid: 0ff8da8a-d3d3-4a15-8103-4fe6ec307427
ms.tgt_platform: multiple
keywords:
- 類別顯示名稱廣告，圖示
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efe3548daa223cdfa05dee8ec3df8f2f8bc800c5ba7449920744de1a67ac8745
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022599"
---
# <a name="class-icons"></a>類別圖示

用來代表類別物件的圖示可以在 DisplaySpecifiers 容器的 **>iconpath** 屬性中指定。 此外，每個類別都可以儲存多個圖示狀態。 例如，資料夾類別可以有開啟、關閉和停用狀態的圖示。 目前的執行最多接受每個類別16個不同的圖示狀態。

**>Iconpath** 屬性可以用兩種方式之一來指定。


```C++
<state>,<icon file name>
```



或


```C++
<state>,<module file name>,<resource ID>
```



在這些範例中，「 &lt; 狀態」 &gt; 是一個整數，其值介於0到15之間。 值0會定義為圖示的預設或關閉狀態。 值1定義為圖示的開啟狀態。 值2是停用的狀態。 所有其他值都是由應用程式定義。

「 &lt; 圖示檔名稱」 &gt; 是包含圖示影像的圖示檔案的路徑和檔案名。

「 &lt; 模組檔案名」 &gt; 是模組（例如 EXE 或 DLL）的路徑和檔案名，其中包含資源中的圖示影像。 「 &lt; 資源識別碼」 &gt; 是一個整數，可指定模組內圖示資源的資源識別碼。

## <a name="adding-a-value-to-the-iconpath-attribute"></a>將值加入至 **>iconpath** 屬性

若要將值新增至 **>iconpath** 屬性，請執行下列步驟。

1.  判斷屬性的值是否存在。 如果要取代某個值，請先使用 [**IADs：:P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) 方法來刪除現有的值，並將 *lnControlCode* 參數設定為 **ADS \_ PROPERTY \_ delete** ，並將 *vProp* 參數設定為要移除的值。 請勿使用 *lnControlCode* 的 **ads \_ 屬性 \_ CLEAR** 或 **ads \_ 屬性 \_ 更新**。
2.  建立代表屬性圖示資料的字串。 如需範例，請參閱上面的格式。
3.  若要加入新的值，請使用 [**IADs：:P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) 方法，並將 *lnControlCode* 參數設定為 [ **ADS] 屬性 [ \_ \_ 附加**]。
4.  若要認可目錄的變更，請呼叫 [**IADs：： SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo)。

 

 