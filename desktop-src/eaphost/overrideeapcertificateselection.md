---
title: OverrideEAPCertificateSelection
description: OverrideEAPCertificateSelection 登錄機碼會判斷用戶端是否會覆寫預設的智慧卡憑證選取行為，並為使用者提供更多可供選擇的憑證。
ms.assetid: 469FECA9-FF2A-46B1-9370-0FF28EF2FB33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d958eeeffba96e7a060ee4dd3edaf8a9935a15d1
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "103841740"
---
# <a name="overrideeapcertificateselection"></a><span data-ttu-id="ea78f-103">OverrideEAPCertificateSelection</span><span class="sxs-lookup"><span data-stu-id="ea78f-103">OverrideEAPCertificateSelection</span></span>

<span data-ttu-id="ea78f-104">OverrideEAPCertificateSelection 登錄機碼會判斷用戶端是否會覆寫預設的智慧卡憑證選取行為，並為使用者提供更多可供選擇的憑證。</span><span class="sxs-lookup"><span data-stu-id="ea78f-104">The OverrideEAPCertificateSelection registry key determines whether the client will override the default smart card certificate selection behavior and provide the user with more certificates to choose from.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="ea78f-105">登錄項目</span><span class="sxs-lookup"><span data-stu-id="ea78f-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   OverrideEAPCertificateSelection = value
```

## <a name="remarks"></a><span data-ttu-id="ea78f-106">備註</span><span class="sxs-lookup"><span data-stu-id="ea78f-106">Remarks</span></span>

<span data-ttu-id="ea78f-107">這是 **REG \_ 二進位** 值。</span><span class="sxs-lookup"><span data-stu-id="ea78f-107">This is a **REG\_BINARY** value.</span></span>



| <span data-ttu-id="ea78f-108">值</span><span class="sxs-lookup"><span data-stu-id="ea78f-108">Value</span></span> | <span data-ttu-id="ea78f-109">描述</span><span class="sxs-lookup"><span data-stu-id="ea78f-109">Description</span></span>                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea78f-110">0x000</span><span class="sxs-lookup"><span data-stu-id="ea78f-110">0x000</span></span> | <span data-ttu-id="ea78f-111">請勿覆寫預設行為。</span><span class="sxs-lookup"><span data-stu-id="ea78f-111">Do not override the default behavior.</span></span>                                                                                                                                                                |
| <span data-ttu-id="ea78f-112">0x001</span><span class="sxs-lookup"><span data-stu-id="ea78f-112">0x001</span></span> | <span data-ttu-id="ea78f-113">從智慧卡選擇最後一個附加的憑證。</span><span class="sxs-lookup"><span data-stu-id="ea78f-113">Choose the last attached certificate from the smart card.</span></span>                                                                                                                                            |
| <span data-ttu-id="ea78f-114">0x010</span><span class="sxs-lookup"><span data-stu-id="ea78f-114">0x010</span></span> | <span data-ttu-id="ea78f-115">顯示智慧卡憑證選取 UI 中的所有憑證。</span><span class="sxs-lookup"><span data-stu-id="ea78f-115">Shows all certificates in the certificate selection UI from the smart card.</span></span>                                                                                                                          |
| <span data-ttu-id="ea78f-116">0x100</span><span class="sxs-lookup"><span data-stu-id="ea78f-116">0x100</span></span> | <span data-ttu-id="ea78f-117">顯示登錄中憑證選取 UI 的所有憑證。</span><span class="sxs-lookup"><span data-stu-id="ea78f-117">Shows all certificates in the certificate selection UI from the registry.</span></span>                                                                                                                            |
| <span data-ttu-id="ea78f-118">0x101</span><span class="sxs-lookup"><span data-stu-id="ea78f-118">0x101</span></span> | <span data-ttu-id="ea78f-119">從登錄中顯示憑證選取 UI 中的所有憑證，以及智慧卡上最後附加的憑證。</span><span class="sxs-lookup"><span data-stu-id="ea78f-119">Shows all certificates in the certificate selection UI from the registry and the last attached certificate from the smart card.</span></span> <span data-ttu-id="ea78f-120">顯示已選取的智慧卡最後附加的憑證。</span><span class="sxs-lookup"><span data-stu-id="ea78f-120">Shows the last attached certificate from the smart card as selected.</span></span> |
| <span data-ttu-id="ea78f-121">0x110</span><span class="sxs-lookup"><span data-stu-id="ea78f-121">0x110</span></span> | <span data-ttu-id="ea78f-122">從登錄和智慧卡顯示憑證選取 UI 中的所有憑證。</span><span class="sxs-lookup"><span data-stu-id="ea78f-122">Shows all certificates in the certificate selection UI from the registry and the smart card.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="ea78f-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="ea78f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea78f-124">EAPHost 登錄設定</span><span class="sxs-lookup"><span data-stu-id="ea78f-124">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




