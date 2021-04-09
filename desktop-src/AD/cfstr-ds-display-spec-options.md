---
title: 'CFSTR_DS_DISPLAY_SPEC_OPTIONS (DSClient) '
description: CFSTR \_ DS \_ 顯示 \_ 規格 \_ 選項剪貼簿格式提供包含 DSDISPLAYSPECOPTIONS 結構的 HGLOBAL。
ms.assetid: 98e033e4-14fe-44ed-83d5-a97e00ecce4c
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DS_DISPLAY_SPEC_OPTIONS
- CFSTR_DSDISPLAYSPECOPTIONS
api_location:
- DSClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d81f3a229971be5ecfb9ec2c86e166af27f94e01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024941"
---
# <a name="cfstr_ds_display_spec_options"></a><span data-ttu-id="5be75-103">CFSTR \_ DS \_ 顯示器 \_ 規格 \_ 選項</span><span class="sxs-lookup"><span data-stu-id="5be75-103">CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS</span></span>

<dl> <dt>

<span data-ttu-id="5be75-104"><span id="CFSTR_DS_DISPLAY_SPEC_OPTIONS"></span><span id="cfstr_ds_display_spec_options"></span>**CFSTR \_ DS \_ 顯示器 \_ 規格 \_ 選項**</span><span class="sxs-lookup"><span data-stu-id="5be75-104"><span id="CFSTR_DS_DISPLAY_SPEC_OPTIONS"></span><span id="cfstr_ds_display_spec_options"></span>**CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5be75-105">"DsDisplaySpecOptions"</span><span class="sxs-lookup"><span data-stu-id="5be75-105">"DsDisplaySpecOptions"</span></span>
</dt> <dt>



<span data-ttu-id="5be75-106">Active Directory 消費者和電腦、Active Directory 的網站和服務，以及 Active Directory 網域及信任] 嵌入式管理單元，都支援 **CFSTR \_ DS \_ 顯示 \_ 規格 \_ 選項** 剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="5be75-106">The Active Directory Users and Computers, the Active Directory Sites and Services, and the Active Directory Domains and Trusts snap-ins support the **CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS** clipboard format.</span></span> <span data-ttu-id="5be75-107">**CFSTR \_ DS \_ 顯示 \_ 規格 \_ 選項** 剪貼簿格式提供包含 [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions)結構的 **HGLOBAL** 。</span><span class="sxs-lookup"><span data-stu-id="5be75-107">The **CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS** clipboard format provides an **HGLOBAL** that contains a [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) structure.</span></span> <span data-ttu-id="5be75-108">**DSDISPLAYSPECOPTIONS** 包含延伸模組所使用的設定資料。</span><span class="sxs-lookup"><span data-stu-id="5be75-108">The **DSDISPLAYSPECOPTIONS** contains configuration data for use by the extension.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="5be75-109"><span id="CFSTR_DSDISPLAYSPECOPTIONS"></span><span id="cfstr_dsdisplayspecoptions"></span>**CFSTR \_ DSDISPLAYSPECOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="5be75-109"><span id="CFSTR_DSDISPLAYSPECOPTIONS"></span><span id="cfstr_dsdisplayspecoptions"></span>**CFSTR\_DSDISPLAYSPECOPTIONS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="5be75-110">**CFSTR \_ DSDISPLAYSPECOPTIONS** 剪貼簿格式等同于 **CFSTR \_ DS \_ 顯示 \_ 規格 \_ 選項** 的剪貼簿格式。</span><span class="sxs-lookup"><span data-stu-id="5be75-110">The **CFSTR\_DSDISPLAYSPECOPTIONS** clipboard format is identical to the **CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS** clipboard format.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5be75-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="5be75-111">Requirements</span></span>



| <span data-ttu-id="5be75-112">需求</span><span class="sxs-lookup"><span data-stu-id="5be75-112">Requirement</span></span> | <span data-ttu-id="5be75-113">值</span><span class="sxs-lookup"><span data-stu-id="5be75-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5be75-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5be75-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5be75-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5be75-115">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="5be75-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5be75-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5be75-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5be75-117">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="5be75-118">標頭</span><span class="sxs-lookup"><span data-stu-id="5be75-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="5be75-119"><dt>DSClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="5be75-119"><dt>DSClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5be75-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5be75-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5be75-121">**DSDISPLAYSPECOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="5be75-121">**DSDISPLAYSPECOPTIONS**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions)
</dt> </dl>

 

 





