---
description: 設定 DVD 播放的 HDCP 保護層級，並遵循 DVD 內容管理系統 (CSS) 規則。
ms.assetid: 8d9ecb9b-8528-4b23-ab2f-234ba2cb7ed0
title: 'OPM_SET_PROTECTION_LEVEL_ACCORDING_TO_CSS_DVD (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 971d288367bdc5c59e11bdfd5b86fb233755c95e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114377"
---
# <a name="opm_set_protection_level_according_to_css_dvd"></a><span data-ttu-id="b3399-103">\_ \_ \_ \_ 根據 \_ \_ CSS \_ DVD OPM 設定保護等級</span><span class="sxs-lookup"><span data-stu-id="b3399-103">OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD</span></span>

<span data-ttu-id="b3399-104">設定 DVD 播放的 HDCP 保護層級，並遵循 DVD 內容管理系統 (CSS) 規則。</span><span class="sxs-lookup"><span data-stu-id="b3399-104">Sets the HDCP protection level for DVD playback, following DVD Content Scramble System (CSS) rules.</span></span>



| <span data-ttu-id="b3399-105">需求</span><span class="sxs-lookup"><span data-stu-id="b3399-105">Requirement</span></span> | <span data-ttu-id="b3399-106">值</span><span class="sxs-lookup"><span data-stu-id="b3399-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3399-107">命令 GUID</span><span class="sxs-lookup"><span data-stu-id="b3399-107">Command GUID</span></span> | <span data-ttu-id="b3399-108">\_ \_ \_ \_ 根據 \_ \_ CSS \_ DVD OPM 設定保護等級</span><span class="sxs-lookup"><span data-stu-id="b3399-108">OPM\_SET\_PROTECTION\_LEVEL\_ACCORDING\_TO\_CSS\_DVD</span></span>                                                |
| <span data-ttu-id="b3399-109">輸入資料</span><span class="sxs-lookup"><span data-stu-id="b3399-109">Input data</span></span>   | <span data-ttu-id="b3399-110">[**OPM \_ SET \_ 保護 \_ 層級 \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)結構</span><span class="sxs-lookup"><span data-stu-id="b3399-110">An [**OPM\_SET\_PROTECTION\_LEVEL\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b3399-111">備註</span><span class="sxs-lookup"><span data-stu-id="b3399-111">Remarks</span></span>

<span data-ttu-id="b3399-112">此命令是用來在播放標準 Dvd 時，設定 High-Bandwidth 數位內容保護 (HDCP) 。</span><span class="sxs-lookup"><span data-stu-id="b3399-112">This command is used to set High-Bandwidth Digital Content Protection (HDCP) when playing standard DVDs.</span></span> <span data-ttu-id="b3399-113">不同于 [**OPM \_ SET \_ PROTECTION \_ LEVEL**](opm-set-protection-level.md) 命令，如果因為某些原因而無法設定 HDCP，此命令不會停止播放。</span><span class="sxs-lookup"><span data-stu-id="b3399-113">Unlike the [**OPM\_SET\_PROTECTION\_LEVEL**](opm-set-protection-level.md) command, if HDCP cannot be set for some reason, this command does not stop playback.</span></span> <span data-ttu-id="b3399-114"> (DVD CSS 規則包含適用于玩家的「最大努力」布建 ) 。否則，此命令與 **OPM \_ SET \_ PROTECTION \_ LEVEL** 命令相同。</span><span class="sxs-lookup"><span data-stu-id="b3399-114">(DVD CSS rules contain a "best effort" provision for players.) Otherwise, this command is identical to the **OPM\_SET\_PROTECTION\_LEVEL** command.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3399-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3399-115">Requirements</span></span>



| <span data-ttu-id="b3399-116">需求</span><span class="sxs-lookup"><span data-stu-id="b3399-116">Requirement</span></span> | <span data-ttu-id="b3399-117">值</span><span class="sxs-lookup"><span data-stu-id="b3399-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b3399-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b3399-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b3399-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3399-119">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b3399-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b3399-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b3399-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3399-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b3399-122">標頭</span><span class="sxs-lookup"><span data-stu-id="b3399-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3399-123"><dt>Opmapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="b3399-123"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3399-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b3399-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3399-125">**IOPMVideoOutput：： Configure**</span><span class="sxs-lookup"><span data-stu-id="b3399-125">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="b3399-126">OPM 命令</span><span class="sxs-lookup"><span data-stu-id="b3399-126">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




