---
title: '錯誤碼 (UIAutomationCoreApi .h) '
description: 本主題說明 Microsoft 消費者介面自動化所公開的錯誤碼。
ms.assetid: f7820aa3-908e-426e-851c-84397019d735
topic_type:
- apiref
api_name:
- UIA_E_ELEMENTNOTAVAILABLE
- UIA_E_ELEMENTNOTENABLED
- UIA_E_INVALIDOPERATION
- UIA_E_NOCLICKABLEPOINT
- UIA_E_NOTSUPPORTED
- UIA_E_PROXYASSEMBLYNOTLOADED
- UIA_E_TIMEOUT
api_location:
- UIAutomationCoreApi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaa03746bfb1a5e56fcac8b39d326581159f459
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024520"
---
# <a name="error-codes-uiautomationcoreapih"></a>錯誤碼 (UIAutomationCoreApi .h) 

本主題說明 Microsoft 消費者介面自動化所公開的錯誤碼。 清單會依名稱以字母順序排序。



| 常數/值                                                                                                                                                                                                                                                              | Description                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIA_E_ELEMENTNOTAVAILABLE"></span><span id="uia_e_elementnotavailable"></span><dl> <dt>**UIA \_E \_ ELEMENTNOTAVAILABLE**</dt> <dt>0x80040201</dt> </dl>          | 指出方法是在虛擬化的元素上呼叫，或在已不存在的專案上呼叫，通常是因為它已被終結。 <br/>                                                                                                  |
| <span id="UIA_E_ELEMENTNOTENABLED"></span><span id="uia_e_elementnotenabled"></span><dl> <dt>**UIA \_E \_ ELEMENTNOTENABLED**</dt> <dt>0x80040200</dt> </dl>                | 指出需要已啟用專案的方法（例如 [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select) 或 [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)）是在已停用的元素上呼叫。 <br/>             |
| <span id="UIA_E_INVALIDOPERATION"></span><span id="uia_e_invalidoperation"></span><dl> <dt>**UIA \_E \_ INVALIDOPERATION**</dt> <dt>0x80131509</dt> </dl>                   | 指出方法嘗試的作業無效。<br/>                                                                                                                                                                          |
| <span id="UIA_E_NOCLICKABLEPOINT"></span><span id="uia_e_noclickablepoint"></span><dl> <dt>**UIA \_E \_ NOCLICKABLEPOINT**</dt> <dt>0x80040202</dt> </dl>                   | 表示在沒有可點按點的專案上呼叫 [**GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint) 方法。<br/>                                                                                    |
| <span id="UIA_E_NOTSUPPORTED"></span><span id="uia_e_notsupported"></span><dl> <dt>**UIA \_E \_ NOTSUPPORTED**</dt> <dt>0x80040204</dt> </dl>                               | 指出提供者明確不支援指定的屬性或控制項模式。 消費者介面自動化會將此錯誤碼傳回給呼叫者，而不會嘗試提供預設值或回復至另一個提供者。<br/> |
| <span id="UIA_E_PROXYASSEMBLYNOTLOADED"></span><span id="uia_e_proxyassemblynotloaded"></span><dl> <dt>**UIA \_E \_ PROXYASSEMBLYNOTLOADED**</dt> <dt>0x80040203</dt> </dl> | 指出載入包含用戶端 (proxy) 提供者的元件時發生問題。<br/>                                                                                                                                      |
| <span id="UIA_E_TIMEOUT"></span><span id="uia_e_timeout"></span><dl> <dt>**UIA \_E \_ TIMEOUT**</dt> <dt>0x80131505</dt> </dl>                                                      | 指出分配給進程或作業的時間已過期。<br/>                                                                                                                                                                      |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                             |
| 標頭<br/>                   | <dl> <dt>UIAutomationCoreApi。h</dt> </dl> |



 

 





