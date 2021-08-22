---
description: Wmiadap 是在 Windows 上執行的應用程式，可更新 WMI 儲存機制中的效能資訊。
ms.assetid: 459fe19e-3e2e-4a58-b3e7-75fd285f7389
ms.tgt_platform: multiple
title: wmiadap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35a58de2ca5e678cbbb99f803415572be236f2a545ed149b9ad598fb7f9a4664
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049836"
---
# <a name="wmiadap"></a>wmiadap

Wmiadap 是在 Windows 上執行的應用程式，可更新 WMI 儲存機制中的效能資訊。 一般而言，這可讓開發人員和 IT 系統管理員建立腳本來存取效能資訊，例如應用程式所使用的記憶體數量。 下列主題描述您可以用來控制 wmiadap 如何捕獲資訊的命令列介面。

Wmiadap 是與大部分系統上的作業系統一起安裝，位於 C： \\ Windows \\ System32 \\ wbem 目錄中。 如果您看到有關 wmiadap.exe 的錯誤訊息，請搜尋 [Microsoft 支援服務](https://support.microsoft.com/)。 一般而言，除非另有指示，否則您不應該刪除系統中的 wmiadap.exe。

從效能程式庫傳輸資料以及從 [**win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 和 [**win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) 衍生的類別重新整理，是由 [WmiPerfClass](wmi-providers.md) 和 [WMIPerfInst](wmi-providers.md) 提供者完成。 只有在加入新的效能物件時，WmiPerfClass 提供者才會更新 WMI [效能計數器類別](/windows/desktop/CIMWin32Prov/performance-counter-classes) 。 您仍然可以使用 **/r** 參數執行 Wmiadap，以剖析 Windows Driver Model 驅動程式來建立效能物件。 **/F** 參數仍然會從效能程式庫強制更新 WMI 類別。

您可以在命令提示字元中使用下列參數。

**wmiadap** \[ \] /f \[**/r**\]

## <a name="switches"></a>交換器

<dl> <dt>

<span id="_f"></span><span id="_F"></span>**/f**
</dt> <dd>

剖析系統上的所有效能程式庫，並重新整理衍生自 [**win32 \_ PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) 和 [**win32 \_ PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata)的類別。

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

剖析系統上的所有 Windows Driver Model 驅動程式，以建立效能物件。

</dd> </dl>

## <a name="see-also"></a>另請參閱

<dl> <dt>

[效能程式庫和 WMI](performance-libraries-and-wmi.md)
</dt> <dt>

[**winmgmt**](winmgmt.md)
</dt> </dl>

 

 
