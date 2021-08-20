---
title: OverrideEAPCertificateSelection
description: OverrideEAPCertificateSelection 登錄機碼會判斷用戶端是否會覆寫預設的智慧卡憑證選取行為，並為使用者提供更多可供選擇的憑證。
ms.assetid: 469FECA9-FF2A-46B1-9370-0FF28EF2FB33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93efec6968fb27b0d27d88c696101815f0b48c36c100f78092d5b559d4c0f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085912"
---
# <a name="overrideeapcertificateselection"></a>OverrideEAPCertificateSelection

OverrideEAPCertificateSelection 登錄機碼會判斷用戶端是否會覆寫預設的智慧卡憑證選取行為，並為使用者提供更多可供選擇的憑證。

## <a name="registry-entry"></a>登錄項目

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   OverrideEAPCertificateSelection = value
```

## <a name="remarks"></a>備註

這是 **REG \_ 二進位** 值。



| 值 | 描述                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x000 | 請勿覆寫預設行為。                                                                                                                                                                |
| 0x001 | 從智慧卡選擇最後一個附加的憑證。                                                                                                                                            |
| 0x010 | 顯示智慧卡憑證選取 UI 中的所有憑證。                                                                                                                          |
| 0x100 | 顯示登錄中憑證選取 UI 的所有憑證。                                                                                                                            |
| 0x101 | 從登錄中顯示憑證選取 UI 中的所有憑證，以及智慧卡上最後附加的憑證。 顯示已選取的智慧卡最後附加的憑證。 |
| 0x110 | 從登錄和智慧卡顯示憑證選取 UI 中的所有憑證。                                                                                                         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[EAPHost Registry 設定](eaphost-registry-settings.md)
</dt> </dl>

 

 




