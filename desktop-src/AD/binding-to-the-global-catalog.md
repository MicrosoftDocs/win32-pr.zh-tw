---
title: 系結至通用類別目錄
description: 通用類別目錄是命名空間，其中包含樹系中所有網域的目錄資料。
ms.assetid: c3c131c7-d9dd-4dbd-a909-abd0ffd9f375
ms.tgt_platform: multiple
keywords:
- 系結至通用類別目錄 AD
- 通用類別目錄 AD，系結至
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08fe40b944130f66617b0c111b361ca51cbef126
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023287"
---
# <a name="binding-to-the-global-catalog"></a>系結至通用類別目錄

通用類別目錄是命名空間，其中包含樹系中所有網域的目錄資料。 通用類別目錄包含每個網域目錄的部分複本。 它包含企業樹系中每個物件的專案，但不包含每個物件的所有屬性。 相反地，它只包含指定要包含在通用類別目錄中的屬性。

通用類別目錄儲存在整個企業的特定伺服器上。 只有網域控制站可以做為通用類別目錄伺服器。 系統管理員會使用 Active Directory 的網站和服務管理員，來指出指定的網域控制站是否保留通用類別目錄。

若要使用 ADSI 系結至通用類別目錄，請使用 "GC：" 標記。

有兩種方式可以系結至通用類別目錄，以在樹系中執行搜尋：

-   系結至企業根物件，以搜尋樹系中的所有網域。
-   系結至特定物件，以搜尋該物件和其子系。 例如，如果您系結至樹系中的網域樹狀目錄下有兩個網域的網域，您可以在這三個網域之間進行搜尋。 請注意，要系結之物件的辨別名稱，與用來系結至 "LDAP：" 命名空間的分辨名稱完全相同。 回想一下，「LDAP：」是單一網域的完整複本，而「GC：」是樹系中所有網域的部分複本。

如同 "LDAP：" 的名字，您可以使用無伺服器系結或系結至特定的通用類別目錄伺服器。 如果在目前樹系中搜尋，請使用無伺服器系結。 但是，如果是在另一個樹系中搜尋，請指定要系結的功能變數名稱或通用類別目錄伺服器，如下列範例所示。

使用功能變數名稱進行系結：

``` syntax
GC://fabrikam.com
```

使用伺服器名稱進行系結：

``` syntax
GC://servername
```

您也可以系結至通用類別目錄內的特定物件。 若要系結至 fabrikam 網域中的 sales 物件，請使用下列格式。

``` syntax
GC://fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

或者，若要系結至伺服器上的 sales 物件，請使用下列格式。

``` syntax
GC://servername.fabrikam.com/DC=sales,DC=fabrikam,DC=com
```

**搜尋整個樹系**

1.  系結至通用類別目錄命名空間的根目錄。
2.  列舉通用類別目錄容器。 通用類別目錄容器包含單一物件，可供您用來搜尋整個樹系。
3.  使用容器中的物件來執行搜尋。 在 C/c + + 中，呼叫 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 以取得物件的 [**>idirectorysearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) 指標，讓您可以使用 **>idirectorysearch** 介面來執行搜尋。 在 Visual Basic 中，請使用在您 ADO 查詢中從列舉傳回的物件。

若要列舉網站中的通用類別目錄伺服器，請使用下列篩選字串來執行「cn = <yoursite> ，cn = sites」的 LDAP 子樹搜尋 <DN of the configurationNamingContext> 。

``` syntax
(&(objectCategory=nTDSDSA)(options:1.2.840.113556.1.4.803:=1))
```

此篩選器會使用 LDAP 比對 **\_ \_ 規則 \_ 位 \_ 和** 比對規則運算子 (1.2.840.113556.1.4.803) 來尋找在 **options** 屬性的位元遮罩中設定低序位位的 **nTDSDSA** 物件。 低序位位，對應于 Ntdsapi 中定義的 **NTDSDSA \_ OPT \_ 是 \_ GC** 常數，識別通用類別目錄伺服器的 **NTDSDSA** 物件。 如需相符規則的詳細資訊，請參閱 [搜尋篩選語法](/windows/desktop/ADSI/search-filter-syntax)。

**NTDSDSA** 物件的父系是 server 物件，而伺服器物件的 **DNSHostName** 屬性是通用類別目錄伺服器的 DNS 名稱。

您無法使用 \# 定義常數，例如 **NTDSDSA \_ OPT \_ 是 \_ GC** 和 **LDAP \_ \_ 比對規則 \_ 位 \_ ，以及** 直接在搜尋篩選字串中。 不過，您可以使用這些常數作為函式（例如 swprintf） [**的 \_**](/windows/win32/api/winuser/nf-winuser-wsprintfa) 引數，以將常數值插入篩選字串中。

通用類別目錄不代表整個樹系樹狀結構。 例如，您可能會預期下列程式碼範例會列舉樹系中的所有網域，以及每個網域的所有子物件。 實際上，它實際上是列舉樹系中的所有網域，但是沒有任何列舉的網域物件包含任何子系。 這是通用類別目錄的限制。


```VB
Dim oGC As IADs
Dim oDomain As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomain In oGC
    ' Print the name of the domain.
    Debug.Print oDomain.Name
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomain
        Debug.Print oChild.Name
    Next
Next
```



若要修正這個錯誤，必須系結至每個網域物件，然後列舉每個網域的子物件。 下列程式碼範例會顯示適當的技巧。


```VB
Dim oGC As IADs
Dim oDomainEnum As IADs
Dim oDomainBind As IADs
Dim oChild As IADs

Set oGC = GetObject("GC:")
For Each oDomainEnum In oGC
    ' Print the name of the domain.
    Debug.Print oDomainEnum.Name
    
    ' Bind to the domain.
    Set oDomainBind = GetObject("LDAP://" + oDomainEnum.Name)
    
    ' Enumerate the child objects of the domain.
    For Each oChild In oDomainBind
        Debug.Print oChild.Name
    Next
Next
```



如需示範如何搜尋整個樹系的詳細資訊和程式碼範例，請參閱 [搜尋樹系的範例程式碼](example-code-for-searching-a-forest.md)。

 

 