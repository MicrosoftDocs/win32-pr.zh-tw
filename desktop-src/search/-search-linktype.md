---
description: 指定編目或編制索引時的連結類型。
ms.assetid: 2a0ddb31-df35-4da5-9950-b091cd461556
title: LINKTYPE 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKTYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: e5b2105e8d56a9c8042f341ffc3f24a4d7995f4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998227"
---
# <a name="linktype-enumeration"></a><span data-ttu-id="2c42a-103">LINKTYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="2c42a-103">LINKTYPE enumeration</span></span>

<span data-ttu-id="2c42a-104">\[只有在 Windows XP 和 Windows Server 2003 上才支援 **LINKTYPE** 列舉，因此不應再使用。\]</span><span class="sxs-lookup"><span data-stu-id="2c42a-104">\[The **LINKTYPE** enumeration is supported only on Windows XP and Windows Server 2003, and should no longer be used.\]</span></span>

<span data-ttu-id="2c42a-105">指定編目或編制索引時的連結類型。</span><span class="sxs-lookup"><span data-stu-id="2c42a-105">Specifies the type of link when crawling or indexing.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c42a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c42a-106">Syntax</span></span>


```C++
typedef enum _LINKTYPE { 
  LINKTYPE_URL      = 0x00000000,
  LINKTYPE_CONTENT  = 0x00000001,
  LINKTYPE_RELATED  = 0x00000002
} LINKTYPE;
```



## <a name="constants"></a><span data-ttu-id="2c42a-107">常數</span><span class="sxs-lookup"><span data-stu-id="2c42a-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2c42a-108"><span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**LINKTYPE \_ URL**</span><span class="sxs-lookup"><span data-stu-id="2c42a-108"><span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**LINKTYPE\_URL**</span></span>
</dt> <dd>

<span data-ttu-id="2c42a-109">指定是否應編制 Url 連結類型的索引。</span><span class="sxs-lookup"><span data-stu-id="2c42a-109">Specifies whether the URLs link type should be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="2c42a-110"><span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**LINKTYPE \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="2c42a-110"><span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**LINKTYPE\_CONTENT**</span></span>
</dt> <dd>

<span data-ttu-id="2c42a-111">指定是否應該為連結內容編制索引。</span><span class="sxs-lookup"><span data-stu-id="2c42a-111">Specifies whether the link content should be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="2c42a-112"><span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**LINKTYPE \_ 相關**</span><span class="sxs-lookup"><span data-stu-id="2c42a-112"><span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**LINKTYPE\_RELATED**</span></span>
</dt> <dd>

<span data-ttu-id="2c42a-113">指定相關的連結。</span><span class="sxs-lookup"><span data-stu-id="2c42a-113">Specifies a related link.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c42a-114">備註</span><span class="sxs-lookup"><span data-stu-id="2c42a-114">Remarks</span></span>

<span data-ttu-id="2c42a-115">若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能必須使用 **LINKTYPE** 旗標和下列其他 Api： [**IItemPreviewerExt：： GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) 和 [**IItemPreviewerExt：： GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) 方法，以及 [**LINKINFO**](-search-linkinfo.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="2c42a-115">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **LINKTYPE** flags, and the following other APIs: the [**IItemPreviewerExt::GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) and [**IItemPreviewerExt::GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) methods, and the [**LINKINFO**](-search-linkinfo.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c42a-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c42a-116">Requirements</span></span>



| <span data-ttu-id="2c42a-117">需求</span><span class="sxs-lookup"><span data-stu-id="2c42a-117">Requirement</span></span> | <span data-ttu-id="2c42a-118">值</span><span class="sxs-lookup"><span data-stu-id="2c42a-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2c42a-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c42a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2c42a-120">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c42a-120">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2c42a-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c42a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2c42a-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c42a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




