---
description: 本節提供 WMI 傳回碼、符號常數、常值和描述的清單。 腳本、c + + 應用程式或 Wmic 命令可能會傳回這些程式碼。
ms.assetid: 7ae47482-edf4-4aa4-858a-76e55f3cb0a3
ms.tgt_platform: multiple
title: WMI 傳回碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1454c8efc45085e88f78358346679b5cdcf3d05093318845912d7d5a913d8ecf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995378"
---
# <a name="wmi-return-codes"></a>WMI 傳回碼

本節提供 WMI 傳回碼、符號常數、常值和描述的清單。 腳本、c + + 應用程式或 [**Wmic**](wmic.md) 命令可能會傳回這些程式碼。

如果發生錯誤，WMI 會傳回下列其中一個錯誤碼做為32位值，其中兩個高序位位表示訊息的嚴重性代碼。

<dl> <dt>

<span id="0"></span>0
</dt> <dd>

Success

</dd> <dt>

<span id="1"></span>1
</dt> <dd>

資訊

</dd> <dt>

<span id="2"></span>2
</dt> <dd>

警告

</dd> <dt>

<span id="3"></span>3
</dt> <dd>

錯誤

</dd> </dl>

> [!Note]
>
> 如果 WMI 傳回錯誤訊息，請注意，它們可能不會指出 WMI 服務或 WMI 提供者中的問題。 失敗可能源自于作業系統的其他部分，並透過 WMI 出現錯誤。 在任何情況下，請勿將 WMI 儲存機制刪除為第一個動作，因為刪除存放庫可能會導致系統損毀或已安裝的應用程式。
>
> 若要取得問題來源的詳細資訊，您可以下載並執行[WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en)診斷命令列工具。 這項工具會產生一份報告，通常可以找出問題的來源，並提供如何修正問題的指示。 報表也會協助 Microsoft 支援服務協助您。 您可以在[這裡](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d)下載 WMI Diagnosis Utility。

 

-   [**WMI 錯誤常數**](wmi-error-constants.md)
-   [**WMI 非錯誤常數**](wmi-non-error-constants.md)

 

 



