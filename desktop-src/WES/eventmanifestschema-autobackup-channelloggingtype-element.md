---
title: autoBackup (ChannelLoggingType) 元素
description: 決定當目前的記錄檔達到大小上限時，是否要建立新的記錄檔。
ms.assetid: 708c5d44-d20b-437a-a01f-6182b244c736
keywords:
- autoBackup 元素 EventLog
topic_type:
- apiref
api_name:
- autoBackup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d69c1a1c43be9d2376d94f39b3158e167f7bd13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509433"
---
# <a name="autobackup-channelloggingtype-element"></a><span data-ttu-id="19995-104">autoBackup (ChannelLoggingType) 元素</span><span class="sxs-lookup"><span data-stu-id="19995-104">autoBackup (ChannelLoggingType) Element</span></span>

<span data-ttu-id="19995-105">決定當目前的記錄檔達到大小上限時，是否要建立新的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="19995-105">Determines whether to create a new log file when the current log file reaches its maximum size.</span></span>

``` syntax
<xs:element name="autoBackup"
    type="boolean"
 />
```

<span data-ttu-id="19995-106">**AutoBackup** 元素是由 [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="19995-106">The **autoBackup** element is defined by the [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="19995-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="19995-107">Requirements</span></span>



| <span data-ttu-id="19995-108">需求</span><span class="sxs-lookup"><span data-stu-id="19995-108">Requirement</span></span> | <span data-ttu-id="19995-109">值</span><span class="sxs-lookup"><span data-stu-id="19995-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="19995-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19995-110">Minimum supported client</span></span><br/> | <span data-ttu-id="19995-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19995-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="19995-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19995-112">Minimum supported server</span></span><br/> | <span data-ttu-id="19995-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19995-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="19995-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19995-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="19995-115">**父元素**</span><span class="sxs-lookup"><span data-stu-id="19995-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="19995-116">**記錄 (ChannelType)**</span><span class="sxs-lookup"><span data-stu-id="19995-116">**logging (ChannelType)**</span></span>](eventmanifestschema-logging-channeltype-element.md)
</dt> </dl>

 

 





