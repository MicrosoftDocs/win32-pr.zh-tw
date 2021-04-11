---
description: 停用來源讀取器使用後置處理相機外掛程式。
ms.assetid: 837A6BA8-9C79-4B0A-B40D-C094009BFF2C
title: 'MF_SOURCE_READER_DISABLE_CAMERA_PLUGINS 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7c72529d1cb684c547d283ce7f9ec92782f359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194860"
---
# <a name="mf_source_reader_disable_camera_plugins-attribute"></a><span data-ttu-id="61635-103">MF \_ 來源 \_ 讀取器 \_ 停用 \_ 相機 \_ 外掛程式屬性</span><span class="sxs-lookup"><span data-stu-id="61635-103">MF\_SOURCE\_READER\_DISABLE\_CAMERA\_PLUGINS attribute</span></span>

<span data-ttu-id="61635-104">停用 [來源讀取器](source-reader.md)使用後置處理相機外掛程式。</span><span class="sxs-lookup"><span data-stu-id="61635-104">Disables the use of post-processing camera plug-ins by the [Source Reader](source-reader.md).</span></span>

## <a name="data-type"></a><span data-ttu-id="61635-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="61635-105">Data type</span></span>

<span data-ttu-id="61635-106">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="61635-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="61635-107">備註</span><span class="sxs-lookup"><span data-stu-id="61635-107">Remarks</span></span>

<span data-ttu-id="61635-108">當來源讀取器與影片捕獲來源搭配使用時，會套用此屬性。</span><span class="sxs-lookup"><span data-stu-id="61635-108">This attribute applies when the Source Reader is used with a video capture source.</span></span> <span data-ttu-id="61635-109">如果此屬性為 **TRUE**，則會防止來源讀取器載入相機可能提供的任何後續處理外掛程式。</span><span class="sxs-lookup"><span data-stu-id="61635-109">If this attribute is **TRUE**, it prevents the Source Reader from loading any post-processing plug-ins that the camera might provide.</span></span> <span data-ttu-id="61635-110">否則，來源讀取器預設會載入它們。</span><span class="sxs-lookup"><span data-stu-id="61635-110">Otherwise, by default the Source Reader will load them.</span></span>

<span data-ttu-id="61635-111">這個屬性的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="61635-111">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="61635-112">當您建立來源讀取器時，請設定屬性。</span><span class="sxs-lookup"><span data-stu-id="61635-112">Set the attribute when you create the source reader.</span></span>

## <a name="requirements"></a><span data-ttu-id="61635-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="61635-113">Requirements</span></span>



| <span data-ttu-id="61635-114">需求</span><span class="sxs-lookup"><span data-stu-id="61635-114">Requirement</span></span> | <span data-ttu-id="61635-115">值</span><span class="sxs-lookup"><span data-stu-id="61635-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="61635-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61635-116">Minimum supported client</span></span><br/> | <span data-ttu-id="61635-117">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61635-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="61635-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61635-118">Minimum supported server</span></span><br/> | <span data-ttu-id="61635-119">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61635-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="61635-120">標頭</span><span class="sxs-lookup"><span data-stu-id="61635-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="61635-121"><dt>Mfreadwrite。h</dt></span><span class="sxs-lookup"><span data-stu-id="61635-121"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61635-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61635-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61635-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="61635-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="61635-124">來源讀取器屬性</span><span class="sxs-lookup"><span data-stu-id="61635-124">Source Reader Attributes</span></span>](source-reader-attributes.md)
</dt> </dl>

 

 




