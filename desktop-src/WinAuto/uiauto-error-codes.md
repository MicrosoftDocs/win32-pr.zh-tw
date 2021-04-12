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
# <a name="error-codes-uiautomationcoreapih"></a><span data-ttu-id="46daf-103">錯誤碼 (UIAutomationCoreApi .h) </span><span class="sxs-lookup"><span data-stu-id="46daf-103">Error Codes (UIAutomationCoreApi.h)</span></span>

<span data-ttu-id="46daf-104">本主題說明 Microsoft 消費者介面自動化所公開的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="46daf-104">This topic describes the error codes exposed by Microsoft UI Automation.</span></span> <span data-ttu-id="46daf-105">清單會依名稱以字母順序排序。</span><span class="sxs-lookup"><span data-stu-id="46daf-105">The list is sorted alphabetically by name.</span></span>



| <span data-ttu-id="46daf-106">常數/值</span><span class="sxs-lookup"><span data-stu-id="46daf-106">Constant/value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="46daf-107">Description</span><span class="sxs-lookup"><span data-stu-id="46daf-107">Description</span></span>                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIA_E_ELEMENTNOTAVAILABLE"></span><span id="uia_e_elementnotavailable"></span><dl> <span data-ttu-id="46daf-108"><dt>**UIA \_E \_ ELEMENTNOTAVAILABLE**</dt> <dt>0x80040201</dt></span><span class="sxs-lookup"><span data-stu-id="46daf-108"><dt>**UIA\_E\_ELEMENTNOTAVAILABLE**</dt> <dt>0x80040201</dt></span></span> </dl>          | <span data-ttu-id="46daf-109">指出方法是在虛擬化的元素上呼叫，或在已不存在的專案上呼叫，通常是因為它已被終結。</span><span class="sxs-lookup"><span data-stu-id="46daf-109">Indicates that a method was called on a virtualized element, or on an element that no longer exists, usually because it has been destroyed.</span></span> <br/>                                                                                                  |
| <span id="UIA_E_ELEMENTNOTENABLED"></span><span id="uia_e_elementnotenabled"></span><dl> <span data-ttu-id="46daf-110"><dt>**UIA \_E \_ ELEMENTNOTENABLED**</dt> <dt>0x80040200</dt></span><span class="sxs-lookup"><span data-stu-id="46daf-110"><dt>**UIA\_E\_ELEMENTNOTENABLED**</dt> <dt>0x80040200</dt></span></span> </dl>                | <span data-ttu-id="46daf-111">指出需要已啟用專案的方法（例如 [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select) 或 [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)）是在已停用的元素上呼叫。</span><span class="sxs-lookup"><span data-stu-id="46daf-111">Indicates that a method that requires an enabled element, such as [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select) or [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand), was called on an element that was disabled.</span></span> <br/>             |
| <span id="UIA_E_INVALIDOPERATION"></span><span id="uia_e_invalidoperation"></span><dl> <span data-ttu-id="46daf-112"><dt>**UIA \_E \_ INVALIDOPERATION**</dt> <dt>0x80131509</dt></span><span class="sxs-lookup"><span data-stu-id="46daf-112"><dt>**UIA\_E\_INVALIDOPERATION**</dt> <dt>0x80131509</dt></span></span> </dl>                   | <span data-ttu-id="46daf-113">指出方法嘗試的作業無效。</span><span class="sxs-lookup"><span data-stu-id="46daf-113">Indicates that the method attempted an operation that was not valid.</span></span><br/>                                                                                                                                                                          |
| <span id="UIA_E_NOCLICKABLEPOINT"></span><span id="uia_e_noclickablepoint"></span><dl> <span data-ttu-id="46daf-114"><dt>**UIA \_E \_ NOCLICKABLEPOINT**</dt> <dt>0x80040202</dt></span><span class="sxs-lookup"><span data-stu-id="46daf-114"><dt>**UIA\_E\_NOCLICKABLEPOINT**</dt> <dt>0x80040202</dt></span></span> </dl>                   | <span data-ttu-id="46daf-115">表示在沒有可點按點的專案上呼叫 [**GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint) 方法。</span><span class="sxs-lookup"><span data-stu-id="46daf-115">Indicates that the [**GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint) method was called on an element that has no clickable point.</span></span><br/>                                                                                    |
| <span id="UIA_E_NOTSUPPORTED"></span><span id="uia_e_notsupported"></span><dl> <span data-ttu-id="46daf-116"><dt>**UIA \_E \_ NOTSUPPORTED**</dt> <dt>0x80040204</dt></span><span class="sxs-lookup"><span data-stu-id="46daf-116"><dt>**UIA\_E\_NOTSUPPORTED**</dt> <dt>0x80040204</dt></span></span> </dl>                               | <span data-ttu-id="46daf-117">指出提供者明確不支援指定的屬性或控制項模式。</span><span class="sxs-lookup"><span data-stu-id="46daf-117">Indicates that the provider explicitly does not support the specified property or control pattern.</span></span> <span data-ttu-id="46daf-118">消費者介面自動化會將此錯誤碼傳回給呼叫者，而不會嘗試提供預設值或回復至另一個提供者。</span><span class="sxs-lookup"><span data-stu-id="46daf-118">UI Automation will return this error code to the caller without attempting to provide a default value or falling back to another provider.</span></span><br/> |
| <span id="UIA_E_PROXYASSEMBLYNOTLOADED"></span><span id="uia_e_proxyassemblynotloaded"></span><dl> <span data-ttu-id="46daf-119"><dt>**UIA \_E \_ PROXYASSEMBLYNOTLOADED**</dt> <dt>0x80040203</dt></span><span class="sxs-lookup"><span data-stu-id="46daf-119"><dt>**UIA\_E\_PROXYASSEMBLYNOTLOADED**</dt> <dt>0x80040203</dt></span></span> </dl> | <span data-ttu-id="46daf-120">指出載入包含用戶端 (proxy) 提供者的元件時發生問題。</span><span class="sxs-lookup"><span data-stu-id="46daf-120">Indicates that a problem occurred when loading an assembly that contains a client-side (proxy) provider.</span></span><br/>                                                                                                                                      |
| <span id="UIA_E_TIMEOUT"></span><span id="uia_e_timeout"></span><dl> <span data-ttu-id="46daf-121"><dt>**UIA \_E \_ TIMEOUT**</dt> <dt>0x80131505</dt></span><span class="sxs-lookup"><span data-stu-id="46daf-121"><dt>**UIA\_E\_TIMEOUT**</dt> <dt>0x80131505</dt></span></span> </dl>                                                      | <span data-ttu-id="46daf-122">指出分配給進程或作業的時間已過期。</span><span class="sxs-lookup"><span data-stu-id="46daf-122">Indicates that the time allotted for a process or operation has expired.</span></span><br/>                                                                                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="46daf-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="46daf-123">Requirements</span></span>



| <span data-ttu-id="46daf-124">需求</span><span class="sxs-lookup"><span data-stu-id="46daf-124">Requirement</span></span> | <span data-ttu-id="46daf-125">值</span><span class="sxs-lookup"><span data-stu-id="46daf-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46daf-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46daf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="46daf-127">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46daf-127">Windows XP \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="46daf-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46daf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="46daf-129">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46daf-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="46daf-130">標頭</span><span class="sxs-lookup"><span data-stu-id="46daf-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="46daf-131"><dt>UIAutomationCoreApi。h</dt></span><span class="sxs-lookup"><span data-stu-id="46daf-131"><dt>UIAutomationCoreApi.h</dt></span></span> </dl> |



 

 





