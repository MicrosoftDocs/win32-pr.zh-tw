---
description: 下表說明 IP \_ DSCP \_ 流量 \_ 類型通訊端選項。
ms.assetid: 0042B53F-B84E-453A-8E18-87052280DAD5
title: IP_DSCP_TRAFFIC_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IP_DSCP_TRAFFIC_TYPE
api_type:
- HeaderDef
api_location:
- N/A
ms.openlocfilehash: 80cbe41e58cf36cd366015d83af380f5952630ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990637"
---
# <a name="ip_dscp_traffic_type"></a><span data-ttu-id="ecd60-103">IP \_ DSCP \_ 流量 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="ecd60-103">IP\_DSCP\_TRAFFIC\_TYPE</span></span>

<span data-ttu-id="ecd60-104">下表說明 IP \_ DSCP \_ 流量 \_ 類型通訊端選項。</span><span class="sxs-lookup"><span data-stu-id="ecd60-104">The following table describes IP\_DSCP\_TRAFFIC\_TYPE Socket Options.</span></span>

<dl> <span data-ttu-id="ecd60-105"><dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**IP \_ DSCP \_ 流量 \_ 類型**</dt> </span><span class="sxs-lookup"><span data-stu-id="ecd60-105"><dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**IP\_DSCP\_TRAFFIC\_TYPE**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="ecd60-106">選項</span><span class="sxs-lookup"><span data-stu-id="ecd60-106">Option</span></span>              | <span data-ttu-id="ecd60-107">Get</span><span class="sxs-lookup"><span data-stu-id="ecd60-107">Get</span></span> | <span data-ttu-id="ecd60-108">設定</span><span class="sxs-lookup"><span data-stu-id="ecd60-108">Set</span></span> | <span data-ttu-id="ecd60-109">Optval 類型</span><span class="sxs-lookup"><span data-stu-id="ecd60-109">Optval Type</span></span> | <span data-ttu-id="ecd60-110">Description</span><span class="sxs-lookup"><span data-stu-id="ecd60-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------------|-----|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecd60-111">DSCP \_ 流量 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="ecd60-111">DSCP\_TRAFFIC\_TYPE</span></span> | <span data-ttu-id="ecd60-112">是</span><span class="sxs-lookup"><span data-stu-id="ecd60-112">Yes</span></span> | <span data-ttu-id="ecd60-113">是</span><span class="sxs-lookup"><span data-stu-id="ecd60-113">Yes</span></span> | <span data-ttu-id="ecd60-114">DWORD</span><span class="sxs-lookup"><span data-stu-id="ecd60-114">DWORD</span></span>       | <span data-ttu-id="ecd60-115">藉由將此值設定為 **DSCP \_ 流量 \_ 類型** 中所定義的值，應用程式將能夠根據所要求的服務類型，要求其網路封包被處理。</span><span class="sxs-lookup"><span data-stu-id="ecd60-115">By setting this value to values defined in **DSCP\_TRAFFIC\_TYPE**, an application will be able to ask its network packets to be treated according to the type of service being requested.</span></span> <span data-ttu-id="ecd60-116">同樣地，對 [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) 的呼叫可以用來取得指定之通訊端上所要求的流量類型目前的設定。</span><span class="sxs-lookup"><span data-stu-id="ecd60-116">Similarly calls to [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) can be used to obtain the current setting for the type of traffic requested on the given socket</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ecd60-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ecd60-117">Requirements</span></span>



| <span data-ttu-id="ecd60-118">需求</span><span class="sxs-lookup"><span data-stu-id="ecd60-118">Requirement</span></span> | <span data-ttu-id="ecd60-119">值</span><span class="sxs-lookup"><span data-stu-id="ecd60-119">Value</span></span> |
|----------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="ecd60-120">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ecd60-120">End of client support</span></span><br/> | <span data-ttu-id="ecd60-121">Windows 10</span><span class="sxs-lookup"><span data-stu-id="ecd60-121">Windows 10</span></span><br/>                                                          |
| <span data-ttu-id="ecd60-122">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="ecd60-122">End of server support</span></span><br/> | <span data-ttu-id="ecd60-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ecd60-123">Windows Server 2016</span></span><br/>                                                 |
| <span data-ttu-id="ecd60-124">標頭</span><span class="sxs-lookup"><span data-stu-id="ecd60-124">Header</span></span><br/>                | <dl> <span data-ttu-id="ecd60-125"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="ecd60-125"><dt>N/A</dt></span></span> </dl> |



 

 




