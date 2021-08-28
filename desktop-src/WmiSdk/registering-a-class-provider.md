---
description: 若要建立 WMI 類別提供者，您必須 \_ \_ 使用 ClassProviderRegistration 的實例，註冊代表提供者的 Win32Provider 實例 \_ \_ 。
ms.assetid: ed834969-47e9-47df-9db8-c805b2eb71da
ms.tgt_platform: multiple
title: 註冊類別提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16a28b489f2cfd01163d6b32c9a70c0d8a193a542197795d6d2b40de0e1baef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316480"
---
# <a name="registering-a-class-provider"></a>註冊類別提供者

若要建立 WMI 類別提供者，您必須使用 [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md)的實例，註冊代表提供者的 [**\_ \_ Win32Provider**](--win32provider.md)實例。 如果您是 COM 物件，則您的提供者必須向作業系統和 WMI 註冊。 下列程式假設您已依照 [註冊提供者](registering-a-provider.md)中所述的方式來執行註冊程式。 如果您的提供者將大部分資料儲存在 WMI 存放庫中，而且資料只會在 WMI 初始化時更新，請將您的類別註冊為 push 類別提供者。 如果您所提供的資料經常變更，而且您的程式碼會在每個 WMI 要求時動態抓取，請將您的提供者註冊為提取類別提供者。

下列程式說明如何註冊推播類別提供者。

**註冊推播類別提供者**

-   將 [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md)實例的 **InteractionType** 屬性設定為1。

    建立 [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md)的實例是註冊程式的一部分。

下列程式說明如何註冊提取類別提供者。

**註冊提取類別提供者**

1.  建立描述提供者之 [**\_ \_ Win32Provider**](--win32provider.md)類別的實例。
2.  建立 [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md)類別的實例，以描述提供者的功能集。

    在 [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md)實例中：

    1.  設定 **InteractionType** 屬性，指出提供者是否為 push 或 pull 提供者。
    2.  以 [**動態**](standard-wmi-qualifiers.md) 和 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider) 辨識符號標記類別。

        [**動態**](standard-wmi-qualifiers.md)限定詞表示 WMI 應該使用提供者來取出類別實例。 [**提供者**](/windows/desktop/api/Provider/nl-provider-provider)辨識符號會指定 WMI 應使用的提供者名稱。

    3.  定義 **ResultSetQueries**、 **ReferencedSetQueries** 和 **UnsupportedQueries** 屬性。

        這些查詢屬性會描述有關支援類別的詳細資訊。

除了描述類別的各種支援方法之外， [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md)類別也有三個描述一系列查詢的屬性。 搭配使用時，這三個屬性會描述類別提供者所提供的整個類別範圍。 每個查詢屬性都包含 WQL SELECT 語句（稱為「架構查詢」）來指定支援類別的類型。 架構查詢會指定稱為中繼類別的特殊類別名稱 \_ 。 下表列出查詢屬性。



| 屬性                 | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ResultSetQueries**     | 包含提供者所提供之結果集的相關資訊。 WMI 會使用此資訊來判斷是否要叫用提供者來滿足應用程式的查詢。 這個屬性描述提供者可以提供的所有類別集合，或是可用類別的超集合，但絕對不能是子集。 WMI 需要提供者在這個屬性中指定至少一個查詢。<br/> 下列範例顯示如何在提供者提供參考 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)類別的關聯類別時設定 **ResultSetQueries** 。<br/> `SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"`<br/> 下列範例顯示如何在提供者提供參考其他未知類別的類別時，指定一般查詢。<br/> `SELECT * FROM meta_class`<br/> 下列範例示範當提供者僅提供子類別，而不是指定類別的父類別時，如何設定 **ResultSetQueries** 。<br/> `SELECT * FROM meta_class WHERE __Dynasty = "MyClass"`<br/> 下列範例示範如何使用這個屬性的特殊 \_ \_ 屬性，並在提供者提供所有類別和子類別時設定 **ResultSetQueries** 。<br/> `SELECT * FROM meta_class WHERE __this ISA "MyClass"`<br/> |
| **ReferencedSetQueries** | 決定是否要在要求關聯和參考的架構查詢中略過提供者。 可以提供關聯類別的提供者，在其 **ReferencedSetQueries** 屬性中必須至少包含一個查詢。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **UnsupportedQueries**   | 包含類別提供者未提供之結果集的相關資訊。 WMI 會使用這個屬性來減去 **ResultSetQueries** 所隱含的一組類別。 例如，類別提供者可以針對所有衍生自 MyClass 的類別指定 **ResultSetQueries** 支援，並在 **UnsupportedQueries** 中指定不支援一個特定的衍生類別。<br/> 提供者可註冊其查詢處理功能的詳細資訊，其執行速度愈快。 在 **UnsupportedQueries** 屬性中輸入一或多個查詢是一種特定的方法，當提供者依賴其未提供的類別時，這一點特別重要。 當針對 **UnsupportedQueries** 屬性中的查詢所列的類別提出要求時，WMI 可以提供類別本身，或叫用替代提供者來提供它。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

因為 WMI 不支援或子句，所以您必須為每個類別建立個別的查詢。

當類別提供者提供 MyClass1、MyClass2 和 MyClass3 時，會在 **ResultSetQueries** 中指定下列查詢。


```sql
SELECT * FROM meta_class WHERE __Class = "MyClass1"
SELECT * FROM meta_class WHERE __Class = "MyClass2"
SELECT * FROM meta_class WHERE __Class = "MyClass3"
```



只有系統管理員可以藉由建立 [**\_ \_ Win32Provider**](--win32provider.md)和 [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md)的實例來註冊或刪除提供者。

 

