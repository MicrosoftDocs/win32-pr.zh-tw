---
description: MF_MT_FSSourceTypeDecoded 屬性-指定在設定時間戳記時，解碼器是否可以使用 (DTS) 的解碼時間戳記。
title: MF_MT_FSSourceTypeDecoded
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3799c11e3b921427ff4a3b05aa3d7f47e297ba14
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093086"
---
# <a name="mf_mt_fssourcetypedecoded-attribute"></a><span data-ttu-id="8c8b5-103">MF \_ MT \_ FSSourceTypeDecoded 屬性</span><span class="sxs-lookup"><span data-stu-id="8c8b5-103">MF\_MT\_FSSourceTypeDecoded attribute</span></span>

<span data-ttu-id="8c8b5-104">指定媒體類型為自動解碼。</span><span class="sxs-lookup"><span data-stu-id="8c8b5-104">Specifies that a media type is auto-decoded.</span></span>

## <a name="data-type"></a><span data-ttu-id="8c8b5-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="8c8b5-105">Data type</span></span>

<span data-ttu-id="8c8b5-106">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="8c8b5-106">**BOOL** stored as **UINT32**</span></span>


## <a name="remarks"></a><span data-ttu-id="8c8b5-107">備註</span><span class="sxs-lookup"><span data-stu-id="8c8b5-107">Remarks</span></span>
<span data-ttu-id="8c8b5-108">媒體類型標示為屬性，以指出這不存在於實體來源上，並且由管線合成。</span><span class="sxs-lookup"><span data-stu-id="8c8b5-108">A media type is marked an attribute to indicate this doesn't exist on the physical source and is synthesized by the pipeline.</span></span> <span data-ttu-id="8c8b5-109">值為 1 (TRUE) 表示媒體類型已合成。</span><span class="sxs-lookup"><span data-stu-id="8c8b5-109">A value of 1 (TRUE) indicates that the media type is synthesized.</span></span> <span data-ttu-id="8c8b5-110">值為 0 (FALSE) ，或不存在值，表示它不存在。</span><span class="sxs-lookup"><span data-stu-id="8c8b5-110">A value of 0 (FALSE), or the value not being present, indicates that it is not.</span></span>

<span data-ttu-id="8c8b5-111">在目前的版本中，您應該使用下列 GUID 值（而不是 MD_MT_FSSourceTypeDecoded 常數）來指定這個屬性：</span><span class="sxs-lookup"><span data-stu-id="8c8b5-111">In the current release, this attribute should be specified using the following GUID value rather than the MD_MT_FSSourceTypeDecoded constant:</span></span>

```ea031a62-8bbb-43c5-b5c4-572d2d231c18```


## <a name="requirements"></a><span data-ttu-id="8c8b5-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c8b5-112">Requirements</span></span>



| <span data-ttu-id="8c8b5-113">需求</span><span class="sxs-lookup"><span data-stu-id="8c8b5-113">Requirement</span></span> | <span data-ttu-id="8c8b5-114">值</span><span class="sxs-lookup"><span data-stu-id="8c8b5-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8c8b5-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c8b5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8c8b5-116">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c8b5-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="8c8b5-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c8b5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8c8b5-118">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c8b5-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |



## <a name="see-also"></a><span data-ttu-id="8c8b5-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c8b5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c8b5-120">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="8c8b5-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




