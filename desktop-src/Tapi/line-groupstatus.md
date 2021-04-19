---
description: '\_當應用程式目前有開啟行的代理程式處理常式上發生 ACD 群組的狀態變更時，就會傳送 LINE GROUPSTATUS 訊息。 此訊息是使用 lineProxyMessage 函式所產生。'
ms.assetid: 1f3210fe-a7c8-4cfa-8e36-3a88e93d68bb
title: 'LINE_GROUPSTATUS 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22fec7c4701ee7140c02cede1901ef7998e5b60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992897"
---
# <a name="line_groupstatus-message"></a><span data-ttu-id="4827b-104">行 \_ GROUPSTATUS 訊息</span><span class="sxs-lookup"><span data-stu-id="4827b-104">LINE\_GROUPSTATUS message</span></span>

<span data-ttu-id="4827b-105">當應用程式目前有開啟行的代理程式處理常式上發生 ACD 群組的狀態變更時，就會傳送 **LINE \_ GROUPSTATUS** 訊息。</span><span class="sxs-lookup"><span data-stu-id="4827b-105">The **LINE\_GROUPSTATUS** message is sent when the status of an ACD group changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="4827b-106">此訊息是使用 [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) 函式所產生。</span><span class="sxs-lookup"><span data-stu-id="4827b-106">This message is generated using the [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="4827b-107">參數</span><span class="sxs-lookup"><span data-stu-id="4827b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4827b-108">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="4827b-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="4827b-109">應用程式線路裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4827b-109">The application's handle to the line device.</span></span> <span data-ttu-id="4827b-110">這與代理程式處理常式相關。</span><span class="sxs-lookup"><span data-stu-id="4827b-110">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="4827b-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="4827b-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="4827b-112">開啟行時所提供的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="4827b-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="4827b-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="4827b-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="4827b-114">保留的。</span><span class="sxs-lookup"><span data-stu-id="4827b-114">Reserved.</span></span> <span data-ttu-id="4827b-115">設定為零。</span><span class="sxs-lookup"><span data-stu-id="4827b-115">Set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="4827b-116">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="4827b-116">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="4827b-117">指定已變更的群組狀態。</span><span class="sxs-lookup"><span data-stu-id="4827b-117">Specifies the group status that has changed.</span></span> <span data-ttu-id="4827b-118">應用程式可以叫用 [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) 來判斷可用群組中的變更。</span><span class="sxs-lookup"><span data-stu-id="4827b-118">The application can invoke [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista) to determine the changes in available groups.</span></span> <span data-ttu-id="4827b-119">*DwParam2* 參數是一或多個 [**LINEGROUPSTATUS \_ 常數**](linegroupstatus--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="4827b-119">The *dwParam2* parameter is one or more of the [**LINEGROUPSTATUS\_ constants**](linegroupstatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="4827b-120">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="4827b-120">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="4827b-121">保留的。</span><span class="sxs-lookup"><span data-stu-id="4827b-121">Reserved.</span></span> <span data-ttu-id="4827b-122">設定為零。</span><span class="sxs-lookup"><span data-stu-id="4827b-122">Set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4827b-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="4827b-123">Requirements</span></span>



| <span data-ttu-id="4827b-124">需求</span><span class="sxs-lookup"><span data-stu-id="4827b-124">Requirement</span></span> | <span data-ttu-id="4827b-125">值</span><span class="sxs-lookup"><span data-stu-id="4827b-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4827b-126">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="4827b-126">TAPI version</span></span><br/> | <span data-ttu-id="4827b-127">需要 TAPI 2。2</span><span class="sxs-lookup"><span data-stu-id="4827b-127">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="4827b-128">標頭</span><span class="sxs-lookup"><span data-stu-id="4827b-128">Header</span></span><br/>       | <dl> <span data-ttu-id="4827b-129"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="4827b-129"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4827b-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4827b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4827b-131">**lineGetGroupList**</span><span class="sxs-lookup"><span data-stu-id="4827b-131">**lineGetGroupList**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista)
</dt> </dl>

 

 




