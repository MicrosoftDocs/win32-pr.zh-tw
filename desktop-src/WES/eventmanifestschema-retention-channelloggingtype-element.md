---
title: 保留 (ChannelLoggingType) 元素
description: 判斷記錄檔是否為連續或迴圈的記錄檔。
ms.assetid: a67425a1-275f-4a04-b327-91707f9382c6
keywords:
- 保留元素 EventLog
topic_type:
- apiref
api_name:
- retention
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 561b5d6926e49990e79aebe47c447aa63d35f0d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384018"
---
# <a name="retention-channelloggingtype-element"></a><span data-ttu-id="02bcd-104">保留 (ChannelLoggingType) 元素</span><span class="sxs-lookup"><span data-stu-id="02bcd-104">retention (ChannelLoggingType) Element</span></span>

<span data-ttu-id="02bcd-105">判斷記錄檔是否為連續或迴圈的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="02bcd-105">Determines whether the log file is a sequential or circular log file.</span></span>

``` syntax
<xs:element name="retention"
    type="boolean"
 />
```

<span data-ttu-id="02bcd-106">**保留** 專案是由 [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="02bcd-106">The **retention** element is defined by the [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="02bcd-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="02bcd-107">Requirements</span></span>



| <span data-ttu-id="02bcd-108">需求</span><span class="sxs-lookup"><span data-stu-id="02bcd-108">Requirement</span></span> | <span data-ttu-id="02bcd-109">值</span><span class="sxs-lookup"><span data-stu-id="02bcd-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="02bcd-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02bcd-110">Minimum supported client</span></span><br/> | <span data-ttu-id="02bcd-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02bcd-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="02bcd-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02bcd-112">Minimum supported server</span></span><br/> | <span data-ttu-id="02bcd-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02bcd-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="02bcd-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02bcd-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="02bcd-115">**父元素**</span><span class="sxs-lookup"><span data-stu-id="02bcd-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="02bcd-116">**記錄 (ChannelType)**</span><span class="sxs-lookup"><span data-stu-id="02bcd-116">**logging (ChannelType)**</span></span>](eventmanifestschema-logging-channeltype-element.md)
</dt> </dl>

 

 





