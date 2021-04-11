---
description: 釋放包含路徑之記憶體的多載方法。
audience: developer
ms.assetid: 9164d7b2-15b8-4b73-ab8c-68ed45692ea0
ms.tgt_platform: multiple
title: 'CObjectPathParser：： Free 方法 (ObjPath .h) '
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 86494e569f68d8eff8b691c648ec5e221b28b39d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193876"
---
# <a name="cobjectpathparserfree-methods"></a><span data-ttu-id="b85cd-103">CObjectPathParser：： Free 方法</span><span class="sxs-lookup"><span data-stu-id="b85cd-103">CObjectPathParser::Free methods</span></span>

<span data-ttu-id="b85cd-104">\[[**CObjectPathParser**](/windows/win32/api/objpath/nl-objpath-cobjectpathparser)類別是 WMI 提供者架構的一部分，現在會被視為最終狀態，而且不會對影響這些程式庫的非安全性相關問題提供進一步的開發、增強功能或更新。</span><span class="sxs-lookup"><span data-stu-id="b85cd-104">\[The [**CObjectPathParser**](/windows/win32/api/objpath/nl-objpath-cobjectpathparser) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="b85cd-105">[MI api](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure)應該用於所有新的開發。\]</span><span class="sxs-lookup"><span data-stu-id="b85cd-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="b85cd-106">釋放包含路徑之記憶體的多載方法。</span><span class="sxs-lookup"><span data-stu-id="b85cd-106">An overloaded method that releases the memory that contains the path.</span></span>

### <a name="overload-list"></a><span data-ttu-id="b85cd-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="b85cd-107">Overload list</span></span>



| <span data-ttu-id="b85cd-108">方法</span><span class="sxs-lookup"><span data-stu-id="b85cd-108">Method</span></span>                                                                     | <span data-ttu-id="b85cd-109">描述</span><span class="sxs-lookup"><span data-stu-id="b85cd-109">Description</span></span>                                                                          |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| <span data-ttu-id="b85cd-110">[**免費 (LPWSTR)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(lpwstr))</span><span class="sxs-lookup"><span data-stu-id="b85cd-110">[**Free(LPWSTR)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(lpwstr))</span></span>                     | <span data-ttu-id="b85cd-111">釋放包含未剖析路徑的記憶體。</span><span class="sxs-lookup"><span data-stu-id="b85cd-111">Releases the memory that contains the unparsed path.</span></span><br/>                      |
| <span data-ttu-id="b85cd-112">[**免費 (ParsedObjectPath)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(parsedobjectpath))</span><span class="sxs-lookup"><span data-stu-id="b85cd-112">[**Free(ParsedObjectPath)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(parsedobjectpath))</span></span> | <span data-ttu-id="b85cd-113">釋放包含已剖析路徑之結構的記憶體。</span><span class="sxs-lookup"><span data-stu-id="b85cd-113">Releases the memory that contains the structure that has the parsed path.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b85cd-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b85cd-114">Requirements</span></span>



| <span data-ttu-id="b85cd-115">需求</span><span class="sxs-lookup"><span data-stu-id="b85cd-115">Requirement</span></span> | <span data-ttu-id="b85cd-116">值</span><span class="sxs-lookup"><span data-stu-id="b85cd-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b85cd-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b85cd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b85cd-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b85cd-118">Windows�Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="b85cd-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b85cd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b85cd-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b85cd-120">Windows Server�2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="b85cd-121">標頭</span><span class="sxs-lookup"><span data-stu-id="b85cd-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b85cd-122"><dt>ObjPath (包含 ObjPath) </dt></span><span class="sxs-lookup"><span data-stu-id="b85cd-122"><dt>ObjPath.h (include ObjPath.h)</dt></span></span> </dl>                                                      |
| <span data-ttu-id="b85cd-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="b85cd-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="b85cd-124"><dt>FrameDyn .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b85cd-124"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="b85cd-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b85cd-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b85cd-126"><dt>FrameDynOS.dll;</dt><dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b85cd-126"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b85cd-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b85cd-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b85cd-128">**CObjectPathParser**</span><span class="sxs-lookup"><span data-stu-id="b85cd-128">**CObjectPathParser**</span></span>](/windows/win32/api/objpath/nl-objpath-cobjectpathparser)
</dt> </dl>

<span data-ttu-id="b85cd-129">�</span><span class="sxs-lookup"><span data-stu-id="b85cd-129">�</span></span>

<span data-ttu-id="b85cd-130">�</span><span class="sxs-lookup"><span data-stu-id="b85cd-130">�</span></span>
