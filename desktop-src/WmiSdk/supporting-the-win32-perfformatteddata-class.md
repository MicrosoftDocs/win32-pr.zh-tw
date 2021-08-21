---
description: 撰寫從 Win32 PerfFormattedData 衍生類別的高效能提供者時 \_ ，您必須遵循特定慣例，讓 WMI 可以計算屬性值。
ms.assetid: 57912f6f-45ca-491c-8a6c-77e2a6937ccc
ms.tgt_platform: multiple
title: 支援 Win32_PerfFormattedData 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bbed50bde7ef16f6362d28151744cf22d66e5d0f56df253ad48ab469b397d0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050126"
---
# <a name="supporting-the-win32_perfformatteddata-class"></a>支援 Win32 \_ PerfFormattedData 類別

撰寫從 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)衍生類別的高效能提供者時，您必須遵循特定慣例，讓 WMI 可以計算屬性值。

> [!Note]  
> 不建議在任何版本的 Windows 作業系統上撰寫 WMI 高效能提供者來建立效能計數器。 如需詳細資訊，請參閱 [讓執行個體提供者成為 High-Performance 提供者](making-an-instance-provider-into-a-high-performance-provider.md)和 [效能程式庫和 WMI](performance-libraries-and-wmi.md)。

 

下列程式描述如何支援 Win32 \_ PerfFormattedData 類別。

**支援 Win32 \_ PerfFormattedData 類別**

1.  在與對應的原始類別相同的命名空間中建立您的類別。 類別必須衍生自 [**Win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) ，並將 **HiPerf** 辨識符號設定為 **TRUE**。 如需建立自己的 WMI 類別的詳細資訊，請參閱 [設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)。
2.  \_在 [**提供者**](class-qualifiers-for-performance-counter-classes.md)辨識符號中指定 "HiPerfCooker v1"。
3.  除了用於原始類別的限定詞之外，請指定下列類別層級限定詞：

    -   [**AutoCook**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Autocook \_ RawClass**](class-qualifiers-for-performance-counter-classes.md)
    -   [**熟**](class-qualifiers-for-performance-counter-classes.md)
    -   [**昂貴**](class-qualifiers-for-performance-counter-classes.md)
    -   [**動態**](dynamic-qualifier.md)
    -   [**HiPerf**](class-qualifiers-for-performance-counter-classes.md)
    -   [**Locale**](class-qualifiers-for-performance-counter-classes.md)
    -   [**PerfDefault**](class-qualifiers-for-performance-counter-classes.md)
    -   [**提供者**](class-qualifiers-for-performance-counter-classes.md)
    -   [**單身 人士**](standard-wmi-qualifiers.md)

    > [!Note]  
    > 請勿為 **GenericPerfCtr**、 **PerfIndex** 或 **HelpIndex** 設定任何值，因為 ADAP 進程會設定這些值。 如需詳細資訊，請參閱 [**效能計數器類別的類別限定詞**](class-qualifiers-for-performance-counter-classes.md)。

     

4.  在您的類別中包含名為 **Name** 的索引鍵屬性 (單一類別) 不需要此屬性。

    **Name** 屬性的值必須與對應的原始類別相同。 您不能在類別上使用 **名稱** 以外的任何索引鍵屬性。

5.  建立屬性資料類型為 **DWORD** (**Uint32**) 或 **QWORD** (**uint64**) 。

    屬性必須對應至原始類別中的屬性，或是您要建立之類別中的屬性。

6.  除了用於原始類別屬性的 **PerfIndex** 和 **PerfDetail** 限定詞之外，請為類別中的所有屬性指定下列屬性層級限定詞：

    -   [**基本**](property-qualifiers-for-performance-counter-classes.md)
    -   [**CookingType**](property-qualifiers-for-performance-counter-classes.md)
    -   [**計數器**](property-qualifiers-for-performance-counter-classes.md)
    -   [**PerfTimeStamp**](property-qualifiers-for-performance-counter-classes.md)
    -   [**PerfTimeFreq**](property-qualifiers-for-performance-counter-classes.md)
    -   [**SampleWindow**](property-qualifiers-for-performance-counter-classes.md)

    如需詳細資訊，請參閱 [**效能計數器類別的屬性限定詞**](property-qualifiers-for-performance-counter-classes.md)。 此外，Winperf 標頭檔包含您可以針對 **PerfDetail** 和 **CounterType** 指定的值。

7.  請確定您的提供者符合 [效能需求](#performance-requirements)。

## <a name="performance-requirements"></a>效能需求

當您撰寫高效能的提供者時，其效能必須符合下列需求：

-   開啟高效能 DLL 檔案的時間不能超過100毫秒。 整體來說，開啟每個高效能提供者和效能程式庫的速度不能超過5秒。
-   每次收集時，資料重新整理不會超過10毫秒。 在整體重新整理和收集作業中，所有高效能的提供者都不能超過800毫秒的時間。
-   所有高效能提供者的整體 CPU 負載，都不能以互動方式超過 6-7% CPU 負擔，也不能以5% 來進行記錄。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[讓執行個體提供者成為 High-Performance 提供者](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 
