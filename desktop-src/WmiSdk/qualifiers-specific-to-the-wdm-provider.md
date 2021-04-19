---
description: 當從 WNODEs 中解壓縮資料以產生 WDM 驅動程式類別的實例時，設備磁碟機 MOF 檔案中的 WDM 提供者會使用下列限定詞。
ms.assetid: 11b0af59-979f-4908-baef-c9ec564b3cfd
ms.tgt_platform: multiple
title: WDM 提供者專用的限定詞
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: be2bc4593c19555dd5a851de89a1dc2e5db00596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993010"
---
# <a name="qualifiers-specific-to-the-wdm-provider"></a>WDM 提供者專用的限定詞

當從 WNODEs 中解壓縮資料以產生 WDM 驅動程式類別的實例時，設備磁碟機 MOF 檔案中的 [WDM 提供者](/windows/desktop/WmiCoreProv/wdm-provider) 會使用下列限定詞。

<dt>

<span id="MissingValue"></span><span id="missingvalue"></span><span id="MISSINGVALUE"></span>**MissingValue**
</dt> <dd>

資料類型： **DWORD、array、uint8、uint16、uint32、sint8、sint16 或 sint32。**

適用物件：屬性

這個屬性的遺漏值應該以 **Null** 表示，而不是 0 (零) 。

</dd> <dt>

<span id="WMIDataId"></span><span id="wmidataid"></span><span id="WMIDATAID"></span>**WMIDataId**
</dt> <dd>

資料類型： **uint32**

適用物件：屬性

屬性之資料 WNODE 中的索引。 WDM 提供者會使用此辨識符號來決定從 WNODE 中解壓縮資料並產生 WMI 類別時，如何格式化資料。 起始值為1。

</dd> <dt>

<span id="WMIExpense"></span><span id="wmiexpense"></span><span id="WMIEXPENSE"></span>**WMIExpense**
</dt> <dd>

資料類型： **uint32**

適用于：類別

指出存取資料區塊的資源成本。 例如，磁片幾何資訊不需要大量資源，因為它可在裝置延伸模組中取得。 磁片讀取/寫入效能較需要大量資源，因為它需要對每個讀取/寫入作業進行額外的工作。 因此， **WMIExpense** 限定詞值會大於磁片讀取/寫入效能。

</dd> <dt>

<span id="WMIMethodId"></span><span id="wmimethodid"></span><span id="WMIMETHODID"></span>**WMIMethodId**
</dt> <dd>

資料類型： **uint32**

適用于：方法

屬性之資料 WNODE 中的索引。 WDM 提供者會使用此辨識符號來決定從 WNODE 中解壓縮資料並產生 WMI 類別時，如何格式化資料。 起始值為1。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



 

