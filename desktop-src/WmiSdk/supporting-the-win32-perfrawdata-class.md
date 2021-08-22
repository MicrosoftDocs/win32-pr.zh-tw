---
description: 撰寫從 Win32 PerfRawData 衍生類別的高效能提供者時 \_ ，您必須遵循特定慣例，讓 WMI 可以提供資料給屬性值。
ms.assetid: 04abb2f9-800f-497a-ac8f-8ef210746273
ms.tgt_platform: multiple
title: 支援 Win32_PerfRawData 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70c9899c88849c70265b019c1d73021c61cae4758c41f462349537bd2e806ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050116"
---
# <a name="supporting-the-win32_perfrawdata-class"></a>支援 Win32 \_ PerfRawData 類別

撰寫從 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata)衍生類別的高效能提供者時，您必須遵循特定慣例，讓 WMI 可以提供資料給屬性值。

> [!Note]  
> 不建議在任何版本的 Windows 作業系統上撰寫 WMI 高效能提供者來建立效能計數器。 如需詳細資訊，請參閱 [讓執行個體提供者成為 High-Performance 提供者](making-an-instance-provider-into-a-high-performance-provider.md)和 [效能程式庫和 WMI](performance-libraries-and-wmi.md)。

 

下列程式說明如何使用高效能提供者來支援 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 類別。

**支援 Win32 \_ PerfRawData 類別**

1.  在根 CIMv2 命名空間中建立您的類別 \\ 。

    類別必須衍生自 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) ，並將 **Hiperf** 辨識符號設定為 **TRUE**。 您也可以將 WDM (驅動程式) 效能資料類別新增至根 \\ wmi 命名空間。 如需建立自己的 WMI 類別的詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)。

2.  在提供者辨識符號中，將提供者指定為 "NT5 \_ GenericPerfProvider \_ V1"。 
3.  指定下列類別層級的限定詞：

    -   **HiPerf**
    -   **地區設定**
    -   **PerfDetail**
    -   **提供者**

    如需詳細資訊，請參閱 [**效能計數器類別的類別限定詞**](class-qualifiers-for-performance-counter-classes.md)。 請勿定義 **GenericPerfCtr** 限定詞，因為它是針對將效能程式庫資料傳輸至 WMI 類別的 ADAP 進程所保留的。

4.  填入適當的 timestamp 和 frequency 屬性，以用來計算計數器類型公式。

    這些屬性是從 [**Win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 繼承而來，如果您要撰寫高效能的提供者，就必須填滿這些屬性，才能在 [系統監視器] 中顯示該類別。

5.  在您的類別中包含名為 **Name** 的索引鍵屬性 (單一類別) 不需要此屬性。

    您不能在類別上使用 **名稱** 以外的任何索引鍵屬性。

6.  建立屬性資料類型為 **DWORD** (**Uint32**) 或 **QWORD** (**uint64**) 。 這些屬性會在傳輸至效能程式庫時成為效能計數器。
7.  針對您類別中的所有屬性指定下列屬性層級限定詞：

    -   **DisplayName**
    -   **CounterType**
    -   **DefaultScale**
    -   **說明**
    -   **PerfDefault**
    -   **PerfDetail**

    如需詳細資訊，請參閱 [**效能計數器類別的屬性限定詞**](property-qualifiers-for-performance-counter-classes.md)。 此外，Winperf 標頭檔包含您可以針對 **PerfDetail** 和 **CounterType** 指定的值。

    WMI 使用 **DisplayName**、 **Locale** 和 **Description** 限定詞進行當地語系化。 您必須將修改過的限定詞新增至 MS \_ 409 (英文) 命名空間，讓系統監視器可以適當地顯示您的類別資料。 這表示您可以藉由新增具有解說文字的 **描述** 辨識符號，並填入 **DisplayName** 值來修改屬性定義。 您也必須將修改過的限定詞新增至類別所支援的任何其他地區設定命名空間。 如果使用者從您未提供修改過的限定詞的地區設定要求資料，WMI 會預設為 MS 409 命名空間中指定的定義 \_ 。

8.  針對具有應基底值之計數器類型的任何屬性，建立基底屬性。

    這個屬性會緊接在屬性之後，並且命名為 * propertyname ***\_ Base**。 例如，在 [**Win32 \_ PerfRawData \_ PerfDisk \_ LogicalDisk**](./retrieving-raw-and-formatted-performance-data.md)類別中 **AvgDiskBytesPerRead** 的 average 屬性，需要名為 **AvgDiskBytesPerRead \_ base** 的基底屬性來計算樣本數。 若要判斷您想要使用的計數器類型是否需要基底屬性，請在 [WMI 效能計數器類型](wmi-performance-counter-types.md)中依名稱或十進位值找出計數器類型。

9.  請確定您的提供者符合 [效能需求](supporting-the-win32-perfformatteddata-class.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[讓執行個體提供者成為 High-Performance 提供者](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
