---
title: DRM_Level
description: DRM \_ 層級是 Windows Media 格式 SDK 在為以 DRM 第1版保護的檔案建立本機授權時所設定的授權屬性。
ms.assetid: 05357378-4d73-48df-a3b5-bdb2c543ec66
keywords:
- DRM_Level windows Media 格式
topic_type:
- apiref
api_name:
- DRM_Level
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3177197b9c149c2fca2c7678a8fe03c6b412e2d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314349"
---
# <a name="drm_level"></a><span data-ttu-id="65c34-104">DRM \_ 層級</span><span class="sxs-lookup"><span data-stu-id="65c34-104">DRM\_Level</span></span>

<span data-ttu-id="65c34-105">**DRM \_層級** 是 Windows Media 格式 SDK 在為以 DRM 第1版保護的檔案建立本機授權時所設定的授權屬性。</span><span class="sxs-lookup"><span data-stu-id="65c34-105">**DRM\_Level** is a license attribute that the Windows Media Format SDK sets when it creates a local license for files protected with DRM version 1.</span></span> <span data-ttu-id="65c34-106">它包含呼叫應用程式必須有才能存取檔案內容的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="65c34-106">It contains the security level that the calling application must have to access the content in the file.</span></span> <span data-ttu-id="65c34-107">預設值為 150。</span><span class="sxs-lookup"><span data-stu-id="65c34-107">The default value is 150.</span></span>

## <a name="global-constant"></a><span data-ttu-id="65c34-108">全域常數</span><span class="sxs-lookup"><span data-stu-id="65c34-108">Global Constant</span></span>

<span data-ttu-id="65c34-109">g \_ wszWMDRM \_ 層級</span><span class="sxs-lookup"><span data-stu-id="65c34-109">g\_wszWMDRM\_Level</span></span>

## <a name="data-type"></a><span data-ttu-id="65c34-110">資料類型</span><span class="sxs-lookup"><span data-stu-id="65c34-110">Data Type</span></span>

<span data-ttu-id="65c34-111">**WMT \_ 類型 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="65c34-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="65c34-112">備註</span><span class="sxs-lookup"><span data-stu-id="65c34-112">Remarks</span></span>

<span data-ttu-id="65c34-113">應用程式的 DRM 安全性層級是由它在編譯時期連結到的特定 wmstubdrm 程式庫所決定。</span><span class="sxs-lookup"><span data-stu-id="65c34-113">An application's DRM security level is determined by the particular wmstubdrm library that it links to at compile time.</span></span> <span data-ttu-id="65c34-114">如需這些安全性層級的詳細資訊，請參閱 [取得所需的 DRM 程式庫](obtaining-the-required-drm-library.md)。</span><span class="sxs-lookup"><span data-stu-id="65c34-114">For more information on these security levels, see [Obtaining the Required DRM Library](obtaining-the-required-drm-library.md).</span></span> <span data-ttu-id="65c34-115">使用 [**IWMHeaderInfo：： SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) 可在使用 DRM 第1版保護 ASF 檔案時設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="65c34-115">Use [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) to set this property when protecting ASF files with DRM version 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="65c34-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65c34-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65c34-117">**DRM 屬性**</span><span class="sxs-lookup"><span data-stu-id="65c34-117">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




