---
description: 下列函式會搭配 Windows 安全性中心使用。
ms.assetid: FC28ACD2-A3C6-42A9-AE59-61892A139FB7
title: Windows 安全性中心函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250d5b3dd7213d9d7f9363ce6b1a83a1e170e01a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846980"
---
# <a name="windows-security-center-functions"></a>Windows 安全性中心函數

下列函式會搭配 Windows 安全性中心使用。

## <a name="in-this-section"></a>本節內容



| 主題                                                                           | 描述                                                                                                                                                                              |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WscGetSecurityProviderHealth**](/windows/desktop/api/Wscapi/nf-wscapi-wscgetsecurityproviderhealth)<br/> | 取得由指定的 [**WSC \_ 安全性 \_ 提供者**](/windows/desktop/api/Wscapi/ne-wscapi-wsc_security_provider) 列舉值所代表之安全性提供者分類的匯總健全狀況狀態。<br/> |
| [**WscRegisterForChanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges)<br/>               | 註冊當 Windows 安全性中心 (WSC) 偵測到可能會影響其中一個安全性提供者之健康情況的變更時，所要執行的回呼函數。<br/>                    |
| [**WscUnRegisterChanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscunregisterchanges)<br/>                 | 取消呼叫 [**WscRegisterForChanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges) 函式所發出的回呼註冊。<br/>                                               |



 

 

 




