---
description: LINEDEVSTATUSFLAGS \_ 位旗標常數描述布林線裝置狀態專案的集合。
ms.assetid: 5fa754d3-07b2-4b75-91ef-1bf961d9fef4
title: 'LINEDEVSTATUSFLAGS_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70745b1a84119af2305cadabd0a39ab5954e5b7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991545"
---
# <a name="linedevstatusflags_-constants"></a><span data-ttu-id="f2e18-103">LINEDEVSTATUSFLAGS \_ 常數</span><span class="sxs-lookup"><span data-stu-id="f2e18-103">LINEDEVSTATUSFLAGS\_ Constants</span></span>

<span data-ttu-id="f2e18-104">**LINEDEVSTATUSFLAGS \_** 位旗標常數描述布林線裝置狀態專案的集合。</span><span class="sxs-lookup"><span data-stu-id="f2e18-104">The **LINEDEVSTATUSFLAGS\_** bit-flag constants describe a collection of Boolean line device status items.</span></span>

<dl> <dt>

<span data-ttu-id="f2e18-105"><span id="LINEDEVSTATUSFLAGS_CONNECTED"></span><span id="linedevstatusflags_connected"></span>**LINEDEVSTATUSFLAGS \_ 已連線**</span><span class="sxs-lookup"><span data-stu-id="f2e18-105"><span id="LINEDEVSTATUSFLAGS_CONNECTED"></span><span id="linedevstatusflags_connected"></span>**LINEDEVSTATUSFLAGS\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2e18-106">指定線路是否連接至 TAPI。</span><span class="sxs-lookup"><span data-stu-id="f2e18-106">Specifies whether the line is connected to TAPI.</span></span> <span data-ttu-id="f2e18-107">若 **為 TRUE**，表示線路已連線，且 TAPI 能夠線上路裝置上運作。</span><span class="sxs-lookup"><span data-stu-id="f2e18-107">If **TRUE**, the line is connected and TAPI is able to operate on the line device.</span></span> <span data-ttu-id="f2e18-108">如果 **為 FALSE**，則表示該行已中斷連線，而且應用程式無法透過 TAPI 控制線路裝置。</span><span class="sxs-lookup"><span data-stu-id="f2e18-108">If **FALSE**, the line is disconnected and the application is unable to control the line device through TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2e18-109"><span id="LINEDEVSTATUSFLAGS_INSERVICE"></span><span id="linedevstatusflags_inservice"></span>**LINEDEVSTATUSFLAGS \_ INSERVICE**</span><span class="sxs-lookup"><span data-stu-id="f2e18-109"><span id="LINEDEVSTATUSFLAGS_INSERVICE"></span><span id="linedevstatusflags_inservice"></span>**LINEDEVSTATUSFLAGS\_INSERVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2e18-110">指出該行是否為服務。</span><span class="sxs-lookup"><span data-stu-id="f2e18-110">Indicates whether the line is in service.</span></span> <span data-ttu-id="f2e18-111">若 **為 TRUE**，則為服務中的行;如果 **為 FALSE**，則表示該行不在服務中。</span><span class="sxs-lookup"><span data-stu-id="f2e18-111">If **TRUE**, the line is in service; if **FALSE**, the line is out of service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2e18-112"><span id="LINEDEVSTATUSFLAGS_LOCKED"></span><span id="linedevstatusflags_locked"></span>**LINEDEVSTATUSFLAGS 已 \_ 鎖定**</span><span class="sxs-lookup"><span data-stu-id="f2e18-112"><span id="LINEDEVSTATUSFLAGS_LOCKED"></span><span id="linedevstatusflags_locked"></span>**LINEDEVSTATUSFLAGS\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2e18-113">指出行是否已鎖定或解除鎖定。</span><span class="sxs-lookup"><span data-stu-id="f2e18-113">Indicates whether the line is locked or unlocked.</span></span> <span data-ttu-id="f2e18-114">這位最常用於與行動電話相關聯的線路裝置。</span><span class="sxs-lookup"><span data-stu-id="f2e18-114">This bit is most often used with line devices associated with cellular phones.</span></span> <span data-ttu-id="f2e18-115">許多行動電話都有一個安全性機制，需要輸入密碼才能讓電話撥打電話。</span><span class="sxs-lookup"><span data-stu-id="f2e18-115">Many cellular phones have a security mechanism that requires the entry of a password to enable the phone to place calls.</span></span> <span data-ttu-id="f2e18-116">此位可用來向應用程式指出電話已鎖定，而且在手機的使用者介面上輸入密碼之前無法撥打電話，讓應用程式可以向使用者呈現適當的警示。</span><span class="sxs-lookup"><span data-stu-id="f2e18-116">This bit can be used to indicate to applications that the phone is locked and cannot place calls until the password is entered on the user interface of the phone so that the application can present an appropriate alert to the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f2e18-117"><span id="LINEDEVSTATUSFLAGS_MSGWAIT"></span><span id="linedevstatusflags_msgwait"></span>**LINEDEVSTATUSFLAGS \_ MSGWAIT**</span><span class="sxs-lookup"><span data-stu-id="f2e18-117"><span id="LINEDEVSTATUSFLAGS_MSGWAIT"></span><span id="linedevstatusflags_msgwait"></span>**LINEDEVSTATUSFLAGS\_MSGWAIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f2e18-118">指出該行是否有等候中的訊息。</span><span class="sxs-lookup"><span data-stu-id="f2e18-118">Indicates whether the line has a message waiting.</span></span> <span data-ttu-id="f2e18-119">若 **為 TRUE**，則表示訊息正在等候;如果 **為 FALSE**，則表示沒有訊息正在等候。</span><span class="sxs-lookup"><span data-stu-id="f2e18-119">If **TRUE**, a message is waiting; if **FALSE**, no message is waiting.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2e18-120">備註</span><span class="sxs-lookup"><span data-stu-id="f2e18-120">Remarks</span></span>

<span data-ttu-id="f2e18-121">無延伸。</span><span class="sxs-lookup"><span data-stu-id="f2e18-121">No extensibility.</span></span> <span data-ttu-id="f2e18-122">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="f2e18-122">All 32 bits are reserved.</span></span>

<span data-ttu-id="f2e18-123">LINEDEVSTATUSFLAGS \_ 常數用於 [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)資料結構的 **dwDevStatusFlags** 成員內。</span><span class="sxs-lookup"><span data-stu-id="f2e18-123">LINEDEVSTATUSFLAGS\_ constants are used within the **dwDevStatusFlags** member of the [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) data structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2e18-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f2e18-124">Requirements</span></span>



| <span data-ttu-id="f2e18-125">需求</span><span class="sxs-lookup"><span data-stu-id="f2e18-125">Requirement</span></span> | <span data-ttu-id="f2e18-126">值</span><span class="sxs-lookup"><span data-stu-id="f2e18-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f2e18-127">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="f2e18-127">TAPI version</span></span><br/> | <span data-ttu-id="f2e18-128">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f2e18-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f2e18-129">標頭</span><span class="sxs-lookup"><span data-stu-id="f2e18-129">Header</span></span><br/>       | <dl> <span data-ttu-id="f2e18-130"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="f2e18-130"><dt>Tapi.h</dt></span></span> </dl> |



 

 




