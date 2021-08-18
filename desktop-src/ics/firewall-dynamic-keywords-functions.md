---
title: 防火牆動態關鍵字函數
description: 防火牆動態關鍵字包含下列功能。
keywords:
- 防火牆動態關鍵字，函數
ms.topic: article
ms.date: 05/13/2021
ms.localizationpriority: low
ms.openlocfilehash: 1aacc30ecac9cddca5f986878da1ff633660152144e8ca2fe1440fdecfd61e3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015648"
---
# <a name="firewall-dynamic-keywords-functions"></a>防火牆動態關鍵字函數

防火牆動態關鍵字包含下列功能。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) | 要求傳遞有關特定動態關鍵字位址 ([FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)) 物件之變更的通知。 |
| [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/FwpmDynamicKeywordUnsubscribe0) | 取消傳遞有關特定動態關鍵字位址 ([FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)) 物件之變更的通知。 |
| [**PFN_FWADDDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) | 您呼叫的服務中進入點的函式指標類型，可加入指定的動態關鍵字位址。 |
| [**PFN_FWDELETEDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0) | 您呼叫的服務中進入點的函式指標型別，可刪除具有指定之識別碼的動態關鍵字位址。 |
| [**PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) | 服務中進入點的函式指標型別，您可以呼叫此方法來依識別碼列舉特定動態關鍵字位址。 |
| [**PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) | 服務中的進入點的函式指標型別，您可以呼叫此型別來列舉動態關鍵字位址。 您可以根據傳入的列舉旗標來要求特定的物件子集。 |
| [**PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) | 服務中進入點的函式指標型別，您可以呼叫此服務中的動態關鍵字位址資料結構。 |
| [**PFN_FWUPDATEDYNAMICKEYWORDADDRESS0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0) | 您所呼叫之服務中進入點的函式指標類型，會以輸入識別碼來更新動態關鍵字位址。 |

## <a name="related-topics"></a>相關主題

* [防火牆動態關鍵字參考](firewall-dynamic-keywords-reference.md)
