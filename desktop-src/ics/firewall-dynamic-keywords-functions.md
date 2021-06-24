---
title: 防火牆動態關鍵字函數
description: 防火牆動態關鍵字包含下列功能。
keywords:
- 防火牆動態關鍵字，函數
ms.topic: article
ms.date: 05/13/2021
ms.localizationpriority: low
ms.openlocfilehash: d086c3aeb3caf7ff85a7fceeec17943c7112a7e0
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2021
ms.locfileid: "112681138"
---
# <a name="firewall-dynamic-keywords-functions"></a><span data-ttu-id="09e4a-104">防火牆動態關鍵字函數</span><span class="sxs-lookup"><span data-stu-id="09e4a-104">Firewall dynamic keywords functions</span></span>

<span data-ttu-id="09e4a-105">防火牆動態關鍵字包含下列功能。</span><span class="sxs-lookup"><span data-stu-id="09e4a-105">Firewall dynamic keywords contains the following functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="09e4a-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="09e4a-106">In this section</span></span>

| <span data-ttu-id="09e4a-107">主題</span><span class="sxs-lookup"><span data-stu-id="09e4a-107">Topic</span></span> | <span data-ttu-id="09e4a-108">描述</span><span class="sxs-lookup"><span data-stu-id="09e4a-108">Description</span></span> |
|-|-|
| [<span data-ttu-id="09e4a-109">**FwpmDynamicKeywordSubscribe0**</span><span class="sxs-lookup"><span data-stu-id="09e4a-109">**FwpmDynamicKeywordSubscribe0**</span></span>](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) | <span data-ttu-id="09e4a-110">要求傳遞有關特定動態關鍵字位址 ([FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)) 物件之變更的通知。</span><span class="sxs-lookup"><span data-stu-id="09e4a-110">Requests the delivery of notifications regarding changes to particular dynamic keyword address ([FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)) objects.</span></span> |
| [<span data-ttu-id="09e4a-111">**FwpmDynamicKeywordUnsubscribe0**</span><span class="sxs-lookup"><span data-stu-id="09e4a-111">**FwpmDynamicKeywordUnsubscribe0**</span></span>](/windows/win32/api/fwpmu/FwpmDynamicKeywordUnsubscribe0) | <span data-ttu-id="09e4a-112">取消傳遞有關特定動態關鍵字位址 ([FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)) 物件之變更的通知。</span><span class="sxs-lookup"><span data-stu-id="09e4a-112">Cancels the delivery of notifications regarding changes to particular dynamic keyword address ([FW_DYNAMIC_KEYWORD_ADDRESS0](/windows/win32/api/netfw/ns-netfw-fw_dynamic_keyword_address0)) objects.</span></span> |
| [<span data-ttu-id="09e4a-113">**PFN_FWADDDYNAMICKEYWORDADDRESS0**</span><span class="sxs-lookup"><span data-stu-id="09e4a-113">**PFN_FWADDDYNAMICKEYWORDADDRESS0**</span></span>](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) | <span data-ttu-id="09e4a-114">您呼叫的服務中進入點的函式指標類型，可加入指定的動態關鍵字位址。</span><span class="sxs-lookup"><span data-stu-id="09e4a-114">Function pointer type of the entry point in the service that you call to add the specified dynamic keyword address.</span></span> |
| [<span data-ttu-id="09e4a-115">**PFN_FWDELETEDYNAMICKEYWORDADDRESS0**</span><span class="sxs-lookup"><span data-stu-id="09e4a-115">**PFN_FWDELETEDYNAMICKEYWORDADDRESS0**</span></span>](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0) | <span data-ttu-id="09e4a-116">您呼叫的服務中進入點的函式指標型別，可刪除具有指定之識別碼的動態關鍵字位址。</span><span class="sxs-lookup"><span data-stu-id="09e4a-116">Function pointer type of the entry point in the service that you call to delete the dynamic keyword address with the specified ID.</span></span> |
| [<span data-ttu-id="09e4a-117">**PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0**</span><span class="sxs-lookup"><span data-stu-id="09e4a-117">**PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0**</span></span>](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) | <span data-ttu-id="09e4a-118">服務中進入點的函式指標型別，您可以呼叫此方法來依識別碼列舉特定動態關鍵字位址。</span><span class="sxs-lookup"><span data-stu-id="09e4a-118">Function pointer type of the entry point in the service that you call to enumerate the specific dynamic keyword addresses by ID.</span></span> |
| [<span data-ttu-id="09e4a-119">**PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0**</span><span class="sxs-lookup"><span data-stu-id="09e4a-119">**PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0**</span></span>](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) | <span data-ttu-id="09e4a-120">服務中的進入點的函式指標型別，您可以呼叫此型別來列舉動態關鍵字位址。</span><span class="sxs-lookup"><span data-stu-id="09e4a-120">Function pointer type of the entry point in the service that you call to enumerate dynamic keyword addresses by type.</span></span> <span data-ttu-id="09e4a-121">您可以根據傳入的列舉旗標來要求特定的物件子集。</span><span class="sxs-lookup"><span data-stu-id="09e4a-121">You can request a particular subset of objects based on the enumeration flags passed in.</span></span> |
| [<span data-ttu-id="09e4a-122">**PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0**</span><span class="sxs-lookup"><span data-stu-id="09e4a-122">**PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0**</span></span>](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) | <span data-ttu-id="09e4a-123">服務中進入點的函式指標型別，您可以呼叫此服務中的動態關鍵字位址資料結構。</span><span class="sxs-lookup"><span data-stu-id="09e4a-123">Function pointer type of the entry point in the service that you call to free dynamic keyword address data structs allocated by the service.</span></span> |
| [<span data-ttu-id="09e4a-124">**PFN_FWUPDATEDYNAMICKEYWORDADDRESS0**</span><span class="sxs-lookup"><span data-stu-id="09e4a-124">**PFN_FWUPDATEDYNAMICKEYWORDADDRESS0**</span></span>](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0) | <span data-ttu-id="09e4a-125">您所呼叫之服務中進入點的函式指標類型，會以輸入識別碼來更新動態關鍵字位址。</span><span class="sxs-lookup"><span data-stu-id="09e4a-125">Function pointer type of the entry point in the service that you call to update the dynamic keyword address with the input ID.</span></span> |

## <a name="related-topics"></a><span data-ttu-id="09e4a-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="09e4a-126">Related topics</span></span>

* [<span data-ttu-id="09e4a-127">防火牆動態關鍵字參考</span><span class="sxs-lookup"><span data-stu-id="09e4a-127">Firewall dynamic keywords reference</span></span>](firewall-dynamic-keywords-reference.md)
