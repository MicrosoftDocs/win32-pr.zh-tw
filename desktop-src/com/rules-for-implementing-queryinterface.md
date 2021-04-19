---
title: 執行 QueryInterface 的規則
description: 執行 QueryInterface 的規則
ms.assetid: 6db17ed8-06e4-4bae-bc26-113176cc7e0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e40c743d5306e7dae79bd55ec2c43c01afe742
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106999593"
---
# <a name="rules-for-implementing-queryinterface"></a>執行 QueryInterface 的規則

有三個主要規則會管理 COM 物件的 [**IUnknown：： QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 方法：

-   物件必須有身分識別。
-   物件實例上的介面集合必須是靜態的。
-   您必須能夠成功地從任何其他介面針對物件上的任何介面進行查詢。

## <a name="objects-must-have-identity"></a>物件必須有身分識別

對於任何指定的物件實例，對具有 IID IUnknown 的 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 呼叫 \_ 都必須一律傳回相同的實體指標值。 這可讓您在任何兩個介面上呼叫 **QueryInterface** 並比較結果，以判斷它們是否指向相同的物件實例。

## <a name="the-set-of-interfaces-on-an-object-instance-must-be-static"></a>物件實例上的介面集合必須是靜態的

透過 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 可在物件上存取的介面集必須是靜態的，而非動態的。 明確地說 ，如果 queryinterface \_ 針對指定的 iid 傳回 S OK，則在相同物件上的後續呼叫中，它永遠不會傳回 e \_ NOINTERFACE; 而如果 **Queryinterface** \_ 傳回指定 iid 的 e NOINTERFACE，則在相同物件上對相同 IID 的後續呼叫絕不能傳回 S \_ ok。

## <a name="it-must-be-possible-to-query-successfully-for-any-interface-on-an-object-from-any-other-interface"></a>您必須能夠成功地從任何其他介面針對物件上的任何介面進行查詢

亦即，假設有下列程式碼：

``` syntax
IA * pA = (some function returning an IA *); 
IB * pB = NULL; 
HRESULT   hr; 
hr = pA->QueryInterface(IID_IB, &pB); 
 
```

適用下列規則：

-   如果您有物件介面的指標，則對相同介面的 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 進行的呼叫必須成功：

    ``` syntax
    pA->QueryInterface(IID_IA, ...) 
     
    ```

-   如果對第二個介面指標的 [**queryinterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 呼叫成功，則從該指標對第一個介面進行的 **queryinterface** 呼叫也必須成功。 如果已成功取得 pB，則下列也必須成功：

    ``` syntax
    pB->QueryInterface(IID_IA, ...) 
     
    ```

-   任何介面都必須能夠查詢物件上的任何其他介面。 如果已成功取得 pB，且您已使用該指標成功查詢第三個介面 (內部) ，您也必須能夠使用第一個指標 pA 來成功查詢內部。 在此情況下，下列順序必須成功：

    ``` syntax
    IC * pC = NULL; 
    hr = pB->QueryInterface(IID_IC, &pC); 
    pA->QueryInterface(IID_IC, ...) 
     
    ```

介面執行必須維持對指定物件上所有介面之未完成指標參考的計數器。 您應該為計數器使用 **不帶正負號的整數** 。

如果用戶端需要知道資源已經釋出，它必須在呼叫 [**IUnknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)之前，在具有較高層級語義的物件上的某個介面中使用方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用和執行 IUnknown](using-and-implementing-iunknown.md)
</dt> </dl>

 

 