---
description: 設定輸出保護機制的保護層級。
ms.assetid: f4e63bf5-0749-4054-9f86-7fd88f2881ad
title: 'OPM_SET_PROTECTION_LEVEL (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17a80fb674c9347dafc3bcf1a62dc4bc909f0471
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974165"
---
# <a name="opm_set_protection_level"></a><span data-ttu-id="dc382-103">OPM \_ SET \_ 保護 \_ 等級</span><span class="sxs-lookup"><span data-stu-id="dc382-103">OPM\_SET\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="dc382-104">設定輸出保護機制的保護層級。</span><span class="sxs-lookup"><span data-stu-id="dc382-104">Sets the protection level for an output protection mechanism.</span></span>



| <span data-ttu-id="dc382-105">需求</span><span class="sxs-lookup"><span data-stu-id="dc382-105">Requirement</span></span> | <span data-ttu-id="dc382-106">值</span><span class="sxs-lookup"><span data-stu-id="dc382-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc382-107">命令 GUID</span><span class="sxs-lookup"><span data-stu-id="dc382-107">Command GUID</span></span> | <span data-ttu-id="dc382-108">OPM \_ SET \_ 保護 \_ 等級</span><span class="sxs-lookup"><span data-stu-id="dc382-108">OPM\_SET\_PROTECTION\_LEVEL</span></span>                                                                         |
| <span data-ttu-id="dc382-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="dc382-109">Input data</span></span>   | <span data-ttu-id="dc382-110">[**OPM \_ SET \_ 保護 \_ 層級 \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)結構</span><span class="sxs-lookup"><span data-stu-id="dc382-110">An [**OPM\_SET\_PROTECTION\_LEVEL\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="dc382-111">備註</span><span class="sxs-lookup"><span data-stu-id="dc382-111">Remarks</span></span>

<span data-ttu-id="dc382-112">某些連接器可支援多重保護機制。</span><span class="sxs-lookup"><span data-stu-id="dc382-112">Some connectors can support multiple protection mechanisms.</span></span> <span data-ttu-id="dc382-113">使用該類型的連接器，您可以將數個保護機制套用至相同的連接器，每個都有不同的設定。</span><span class="sxs-lookup"><span data-stu-id="dc382-113">With that type of connector, you can apply several protection mechanisms to the same connector, with different settings for each.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc382-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc382-114">Requirements</span></span>



| <span data-ttu-id="dc382-115">需求</span><span class="sxs-lookup"><span data-stu-id="dc382-115">Requirement</span></span> | <span data-ttu-id="dc382-116">值</span><span class="sxs-lookup"><span data-stu-id="dc382-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dc382-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc382-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dc382-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc382-118">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="dc382-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc382-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dc382-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc382-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="dc382-121">標頭</span><span class="sxs-lookup"><span data-stu-id="dc382-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc382-122"><dt>Opmapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="dc382-122"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc382-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc382-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc382-124">**IOPMVideoOutput：： Configure**</span><span class="sxs-lookup"><span data-stu-id="dc382-124">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="dc382-125">OPM 命令</span><span class="sxs-lookup"><span data-stu-id="dc382-125">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




