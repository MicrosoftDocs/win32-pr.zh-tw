---
title: 解析函數名稱衝突的範例
description: 本主題說明如何在建立 ADSI 的延伸模組時解決函式名稱衝突。
ms.assetid: 8121f037-3845-44ba-a2cd-8d7f15e0beb2
ms.tgt_platform: multiple
keywords:
- ADSI ADSI，範例程式碼 Visual Basic，解析函數名稱衝突
- 解決函式名稱衝突 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 049f9ce6447bf6d6ead783db3e34f74374333f10
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316465"
---
# <a name="example-for-resolving-function-name-conflicts"></a>解析函數名稱衝突的範例

請考慮下列事項：

-   IADs0 不支援 Func0。
-   IADs1 支援 Func1 和 Func0。
-   IADs2 支援 Func2 和 Func0。

這三個介面都是雙重介面。


```C++
IADs0 : IDispatch
{
    OtherFunc();
}

IADs1 : IDispatch
{
    Func0() 
    Func1();
}

IADs2 : IDispatch
{
    Func0()
    Func2();
}
```




```VB
Dim myInf1 as IADs1
 
myInf1.Func1  ' IADs1::Func1 is invoked using direct vtable access 
 
myInf1.Func2  ' IADs2::Func2 is invoked using GetIDsOfNames/Invoke
```



請注意，雖然 IADs1 不支援 Func2，但 ADSI 用戶端會辨識一個支援模型中所有雙重和分派介面的 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 。 因此，ADSI 用戶端可以使用 myInf1 直接呼叫 Func2，而不需解析支援 Func2 的介面。


```VB
myInf1.Func2
```



IADs1 和 IADs2 都有一個稱為 Func0 的函式，但 IADs1：： Func0 是直接使用 vtable 存取來叫用，因為下列兩項都適用于用戶端：

-   用戶端有一個指向雙重介面 IADs1 物件的指標，該物件具有稱為 Func0 的函式。
-   Visual Basic 支援直接 vtable 存取，並假設資料類型可透過類型程式庫取得。

在下一個程式碼範例中，用戶端有一個 IADs2 的雙重介面指標，而不是 IADs1。 因此，IADs2：： Func0 是使用直接 vtable 存取來叫用的。


```VB
Dim myInf2 as IADs2
Set myInf2 = myInf1 ' Query for pointer to IADs2 
myInf2.Func0
```



同樣地，在下一個程式碼範例中，IADs1 和 IADs2 都有一個稱為 Func0 的函式，但在這裡，用戶端有一個指向雙重介面 IADs0 的指標，該函式沒有稱為 Func0 的函式。 因此，不能執行直接 vtable 存取。 相反地，會呼叫 [**IDispatch：： GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) 和 [**invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) 來叫用 Func0。


```VB
Dim myInfNone as IADs0
Set myInfNone = myInf1    ' The aggregated object that 
   ' supports IADs1 and IADs2.
myInfNone.Func0
```



請考慮下列兩個案例：

-   IADs1 和 IADs2 分別由兩個 COM 元件（Ext1 和 Ext2）來執行。 如果 Ext1 在登錄中 Ext2 之前，則會叫用 IADs1：： Func0。 但是，如果 Ext2 在登錄中最先出現，則會叫用 IADs2：： Func0。
-   如果 IADs1 和 ADs2 是由相同的擴充物件所執行，則一律會由擴充功能的 [**IADsExtension：:P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) 和 [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) 方法來叫用 Func0。

延伸模組開發人員必須判斷如何解決在擴充功能中具有相同名稱之不同雙重 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面的函式或屬性衝突。 [**IADsExtension：:P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames)和 [**PrivateInvoke**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke)方法的執行應該可解決此衝突。 例如，如果您使用 IMyInterface1：： Func1 和 IMyInterface2：： Func1，其中 IMyInterface1 和 IMyInterface2 是相同擴充物件所支援的雙重 **IDispatch** 介面。 **PrivateGetIDsOfNames** 和 **PrivateInvoke** 方法必須決定應一律呼叫的 Func1。

這同樣適用于不同的雙重或 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面中的衝突 dispid。

例如，IMyInterface1. odl 或 IMyInterface1 中的 DISPID IMyInterface1：： Y 是2。 IMyInterface2：： X 的 DISPID 也是 iMyInterface2. odl 中的2。 [**IADsExtension：:P rivategetidsofnames**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) 必須在延伸模組本身內傳回唯一的 dispid，而不是針對兩者傳回相同的 dispid。

ADSI 藉由不支援具有衝突函式或屬性名稱的多個介面，來解決第一個問題。 它會解決第二個問題，方法是將唯一的（位於相同的延伸模組物件內）介面編號新增至 DISPID 未使用的位。

 

 