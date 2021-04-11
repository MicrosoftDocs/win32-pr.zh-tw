---
description: 儲存連結類型的相關資訊，並由 IItemPreviewerExt 介面使用。
ms.assetid: c1d525ea-ee80-49fb-9447-20465b8f8654
title: LINKINFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: de74f7aefb61f12bf85a457e4478aa76f2156410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191205"
---
# <a name="linkinfo-structure"></a><span data-ttu-id="8a843-103">LINKINFO 結構</span><span class="sxs-lookup"><span data-stu-id="8a843-103">LINKINFO structure</span></span>

<span data-ttu-id="8a843-104">\[只有在 Windows XP 和 Windows Server 2003 上才支援 **LINKINFO** 和 [**IItemPreviewerExt**](-search-iitempreviewerext.md) ，而且不應再使用。\]</span><span class="sxs-lookup"><span data-stu-id="8a843-104">\[**LINKINFO** and [**IItemPreviewerExt**](-search-iitempreviewerext.md) are supported only on Windows XP and Windows Server 2003, and should no longer be used.\]</span></span>

<span data-ttu-id="8a843-105">儲存連結類型的相關資訊，並由 [**IItemPreviewerExt**](-search-iitempreviewerext.md) 介面使用。</span><span class="sxs-lookup"><span data-stu-id="8a843-105">Stores information about link types, and is used by the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a843-106">語法</span><span class="sxs-lookup"><span data-stu-id="8a843-106">Syntax</span></span>


```C++
typedef struct _LINKINFO {
  LINKTYPE type;
  BSTR     bstrContentType;
  BSTR     bstrEncoding;
  BSTR     bstrFileExt;
  VARIANT  varData;
  DWORD    dwRelatedParts;
  BSTR     bstrRelatedCid;
  Long     lCodePage;
} LINKINFO;
```



## <a name="members"></a><span data-ttu-id="8a843-107">成員</span><span class="sxs-lookup"><span data-stu-id="8a843-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8a843-108">**type**</span><span class="sxs-lookup"><span data-stu-id="8a843-108">**type**</span></span>
</dt> <dd>

<span data-ttu-id="8a843-109">類型： **[ **LINKTYPE**](-search-linktype.md)**</span><span class="sxs-lookup"><span data-stu-id="8a843-109">Type: **[**LINKTYPE**](-search-linktype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8a843-110">[**LINKTYPE**](-search-linktype.md)常數所指出的編目或索引時所指定的連結類型。</span><span class="sxs-lookup"><span data-stu-id="8a843-110">The type of link specified when crawling or indexing indicated by a [**LINKTYPE**](-search-linktype.md) constant.</span></span>

</dd> <dt>

<span data-ttu-id="8a843-111">**bstrContentType**</span><span class="sxs-lookup"><span data-stu-id="8a843-111">**bstrContentType**</span></span>
</dt> <dd>

<span data-ttu-id="8a843-112">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8a843-112">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="8a843-113">指定內容類型的 **BSTR** 值。</span><span class="sxs-lookup"><span data-stu-id="8a843-113">A **BSTR** value that specifies the content type.</span></span>

</dd> <dt>

<span data-ttu-id="8a843-114">**bstrEncoding**</span><span class="sxs-lookup"><span data-stu-id="8a843-114">**bstrEncoding**</span></span>
</dt> <dd>

<span data-ttu-id="8a843-115">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8a843-115">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="8a843-116">在 Web 服務描述語言中指定的 EncodingStyle 屬性 (WSDL) 檔。</span><span class="sxs-lookup"><span data-stu-id="8a843-116">An EncodingStyle attribute specified in the Web Services Description Language (WSDL) file.</span></span>

</dd> <dt>

<span data-ttu-id="8a843-117">**bstrFileExt**</span><span class="sxs-lookup"><span data-stu-id="8a843-117">**bstrFileExt**</span></span>
</dt> <dd>

<span data-ttu-id="8a843-118">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8a843-118">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="8a843-119">指定副檔名的 **BSTR** 值。</span><span class="sxs-lookup"><span data-stu-id="8a843-119">A **BSTR** value that specifies the file name extension.</span></span>

</dd> <dt>

<span data-ttu-id="8a843-120">**varData**</span><span class="sxs-lookup"><span data-stu-id="8a843-120">**varData**</span></span>
</dt> <dd>

<span data-ttu-id="8a843-121">類型： **VARIANT**</span><span class="sxs-lookup"><span data-stu-id="8a843-121">Type: **VARIANT**</span></span>

</dd> <dd>

<span data-ttu-id="8a843-122">指定變數值的 variant。</span><span class="sxs-lookup"><span data-stu-id="8a843-122">A variant that specifies the variable value.</span></span>

</dd> <dt>

<span data-ttu-id="8a843-123">**dwRelatedParts**</span><span class="sxs-lookup"><span data-stu-id="8a843-123">**dwRelatedParts**</span></span>
</dt> <dd>

<span data-ttu-id="8a843-124">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8a843-124">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8a843-125">指定相關元件的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="8a843-125">A **DWORD** that specifies the related parts.</span></span>

</dd> <dt>

<span data-ttu-id="8a843-126">**bstrRelatedCid**</span><span class="sxs-lookup"><span data-stu-id="8a843-126">**bstrRelatedCid**</span></span>
</dt> <dd>

<span data-ttu-id="8a843-127">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="8a843-127">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="8a843-128">**BSTR** 值，指定 Cid 屬性（非填補的帶正負號的十進位字串）。</span><span class="sxs-lookup"><span data-stu-id="8a843-128">A **BSTR** value that specifies a Cid property, a non-padded, signed decimal string.</span></span>

</dd> <dt>

<span data-ttu-id="8a843-129">**lCodePage**</span><span class="sxs-lookup"><span data-stu-id="8a843-129">**lCodePage**</span></span>
</dt> <dd>

<span data-ttu-id="8a843-130">類型： **Long**</span><span class="sxs-lookup"><span data-stu-id="8a843-130">Type: **Long**</span></span>

</dd> <dd>

<span data-ttu-id="8a843-131">用來編碼字串的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="8a843-131">The code page to use for encoding the string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a843-132">備註</span><span class="sxs-lookup"><span data-stu-id="8a843-132">Remarks</span></span>

<span data-ttu-id="8a843-133">若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 **LINKINFO** 結構和下列 Api： [**IItemPreviewerExt：： GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) 和 [**IItemPreviewerExt：： GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) 方法和 [**LINKTYPE**](-search-linktype.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="8a843-133">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **LINKINFO** structure, and the following APIs: the [**IItemPreviewerExt::GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) and [**IItemPreviewerExt::GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) methods, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a843-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a843-134">Requirements</span></span>



| <span data-ttu-id="8a843-135">需求</span><span class="sxs-lookup"><span data-stu-id="8a843-135">Requirement</span></span> | <span data-ttu-id="8a843-136">值</span><span class="sxs-lookup"><span data-stu-id="8a843-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8a843-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8a843-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8a843-138">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a843-138">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8a843-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8a843-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8a843-140">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a843-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8a843-141">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="8a843-141">Redistributable</span></span><br/>          | <span data-ttu-id="8a843-142">Windows 桌面搜尋 (WDS) 3。0</span><span class="sxs-lookup"><span data-stu-id="8a843-142">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 




