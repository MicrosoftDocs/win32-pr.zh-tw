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
# <a name="windows-security-center-functions"></a><span data-ttu-id="68045-103">Windows 安全性中心函數</span><span class="sxs-lookup"><span data-stu-id="68045-103">Windows Security Center Functions</span></span>

<span data-ttu-id="68045-104">下列函式會搭配 Windows 安全性中心使用。</span><span class="sxs-lookup"><span data-stu-id="68045-104">The following functions are used with Windows Security Center.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="68045-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="68045-105">In this section</span></span>



| <span data-ttu-id="68045-106">主題</span><span class="sxs-lookup"><span data-stu-id="68045-106">Topic</span></span>                                                                           | <span data-ttu-id="68045-107">描述</span><span class="sxs-lookup"><span data-stu-id="68045-107">Description</span></span>                                                                                                                                                                              |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68045-108">**WscGetSecurityProviderHealth**</span><span class="sxs-lookup"><span data-stu-id="68045-108">**WscGetSecurityProviderHealth**</span></span>](/windows/desktop/api/Wscapi/nf-wscapi-wscgetsecurityproviderhealth)<br/> | <span data-ttu-id="68045-109">取得由指定的 [**WSC \_ 安全性 \_ 提供者**](/windows/desktop/api/Wscapi/ne-wscapi-wsc_security_provider) 列舉值所代表之安全性提供者分類的匯總健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="68045-109">Gets the aggregate health state of the security provider categories represented by the specified [**WSC\_SECURITY\_PROVIDER**](/windows/desktop/api/Wscapi/ne-wscapi-wsc_security_provider) enumeration values.</span></span><br/> |
| [<span data-ttu-id="68045-110">**WscRegisterForChanges**</span><span class="sxs-lookup"><span data-stu-id="68045-110">**WscRegisterForChanges**</span></span>](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges)<br/>               | <span data-ttu-id="68045-111">註冊當 Windows 安全性中心 (WSC) 偵測到可能會影響其中一個安全性提供者之健康情況的變更時，所要執行的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="68045-111">Registers a callback function to be run when Windows Security Center (WSC) detects a change that could affect the health of one of the security providers.</span></span><br/>                    |
| [<span data-ttu-id="68045-112">**WscUnRegisterChanges**</span><span class="sxs-lookup"><span data-stu-id="68045-112">**WscUnRegisterChanges**</span></span>](/windows/desktop/api/Wscapi/nf-wscapi-wscunregisterchanges)<br/>                 | <span data-ttu-id="68045-113">取消呼叫 [**WscRegisterForChanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges) 函式所發出的回呼註冊。</span><span class="sxs-lookup"><span data-stu-id="68045-113">Cancels a callback registration that was made by a call to the [**WscRegisterForChanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges) function.</span></span><br/>                                               |



 

 

 




