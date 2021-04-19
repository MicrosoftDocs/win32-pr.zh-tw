---
description: WMI 類別中的屬性會描述受管理物件的相關資料。
ms.assetid: 4046bfc7-9528-4737-ad61-bbb8419d0b51
ms.tgt_platform: multiple
title: 新增 WMI 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bba8944da155ca250edfed0c6e9160f555ba9551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996937"
---
# <a name="adding-a-wmi-property"></a>新增 WMI 屬性

WMI 類別中的屬性會描述受管理物件的相關資料。 例如， **Handle**、 **ProcessId** 和 **PageFaults** 會定義為 [**Win32 \_ process**](/windows/desktop/CIMWin32Prov/win32-process) 類別的屬性，並描述作業系統進程的各個層面。 如需詳細資訊，請參閱 [撰寫屬性提供者](writing-a-property-provider.md)。

## <a name="defining-a-property-in-mof"></a>在 MOF 中定義屬性

WMI 屬性代表物件中的外觀或狀態。 您可以建立屬性，而不是建立只取得和設定值的方法。 例如， [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)的 **NetEnabled** 屬性會顯示是否已啟用或停用介面卡的狀態。 不過， [**Enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) 和 [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) 方法實際上會執行變更介面卡狀態的動作。

屬性必須具有資料類型。 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)屬性 **控制碼** 的資料類型為 **字串**，而 **PageFaults** 的資料類型為 **uint32**。 如果屬性只能有兩個狀態，屬性的資料類型通常會設定為 **布林值**。

屬性也可以是陣列。 例如， [**Win32 \_ 信任者**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)的安全識別碼 (**SID**) 屬性是一個位元組陣列， (包含 SID 的 **uint8**) 。 屬性可以包含内嵌物件，這些物件是對另一個 WMI 類別的一個或多個實例的參考。 任意存取控制清單 **(DACL)** 和系統存取控制清單 **(SACL)** [**win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)的屬性，例如，會描述具有存取權的群組和帳戶的 [**win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) 物件陣列。 **Win32 \_ SecurityDescriptor** 中的 **群組** 屬性包含 **win32 \_ 受信任** 的單一實例的參考。 如需詳細資訊，請參閱 [在類別中内嵌物件](embedded-objects.md)。

屬性可能有數個 [*限定詞*](gloss-q.md)。 這些 [限定詞](wmi-qualifiers.md) 可 [*通用訊息模型 (CIM)*](gloss-c.md) 或 WMI 辨識符號，或可能是特定類型類別的特定類別，例如 [效能計數器](qualifiers-specific-to-wmi-performance-classes.md) 類別限定詞。 限定詞會指定屬性的某些層面，例如，如果它是唯讀的，或是無法在沒有特定許可權的情況下變更。 例如，嘗試寫入 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)**DACL** 屬性的應用程式需要許可權 **SeSecurityPrivilege** 和 **SeRestorePrivilege**。 如需詳細資訊，請參閱 [新增限定詞](adding-a-qualifier.md)。

最後，屬性必須具有名稱。 您可以在標準程式設計實務的範圍內，將屬性命名為任何內容。 不過，有兩個主要例外狀況。 首先，您不能使用任何 MOF 關鍵字（例如 "class"）作為屬性名稱。 其次，您可能不會使用任何 WQL 關鍵字（例如「群組」）作為屬性名稱。 如需 MOF 和 WQL 關鍵字的詳細資訊，請參閱適用于 WMI 的 [Mof 資料類型](mof-data-types.md) 和 [wql (SQL) ](wql-sql-for-wmi.md)。

針對 c + + 和受控物件格式 (MOF) 程式碼，您可以在宣告類別的同時宣告類別的屬性。

**若要定義屬性**

-   在類別描述的大括弧之間，包含屬性資料類型、名稱，以及選擇性的預設值和限定詞。

    ``` syntax
    class MyClass 
    {
        [key] string   strProp;
        sint32         dwProp1 = 21;
        uint32         dwProp2;
    };
    ```

    上述範例中的 MyClass 類別有三個屬性：字元字串、32位帶正負號的整數，以及32位不帶正負號的整數。 每個屬性都會被指派不區分大小寫的名稱和 MOF 資料類型。

    [**金鑰**](key-qualifier.md)辨識符號會將字串屬性定義為可唯一識別類別實例的索引鍵屬性。 如需限定詞的詳細資訊，請參閱 [新增限定詞](adding-a-qualifier.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立類別](creating-a-class.md)
</dt> </dl>

 

 
