---
description: 包含應用程式 IMFSourceOpenMonitor 介面的指標。
ms.assetid: 5b94ae87-91fc-49d6-9355-83327cfdb3f3
title: 'MFPKEY_SourceOpenMonitor 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a49826ee16a733993b9052e12d9e6fcd5003410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115109"
---
# <a name="mfpkey_sourceopenmonitor-property"></a><span data-ttu-id="22909-103">MFPKEY \_ SourceOpenMonitor 屬性</span><span class="sxs-lookup"><span data-stu-id="22909-103">MFPKEY\_SourceOpenMonitor property</span></span>

<span data-ttu-id="22909-104">包含應用程式之 [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="22909-104">Contains a pointer to the application's [**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor) interface.</span></span>



<span data-ttu-id="22909-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="22909-105">Data type</span></span>

<span data-ttu-id="22909-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="22909-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="22909-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="22909-107">PROPVARIANT member</span></span>

<span data-ttu-id="22909-108">**IUnknown** 指標</span><span class="sxs-lookup"><span data-stu-id="22909-108">**IUnknown** pointer</span></span>

<span data-ttu-id="22909-109">VT \_ 不明</span><span class="sxs-lookup"><span data-stu-id="22909-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="22909-110">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="22909-110">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="22909-111">備註</span><span class="sxs-lookup"><span data-stu-id="22909-111">Remarks</span></span>

<span data-ttu-id="22909-112">應用程式可以將此屬性傳遞至來源解析程式，以從網路來源取得事件通知。</span><span class="sxs-lookup"><span data-stu-id="22909-112">Applications can pass this property to the source resolver to get event notifications from the network source.</span></span>

## <a name="requirements"></a><span data-ttu-id="22909-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="22909-113">Requirements</span></span>



| <span data-ttu-id="22909-114">需求</span><span class="sxs-lookup"><span data-stu-id="22909-114">Requirement</span></span> | <span data-ttu-id="22909-115">值</span><span class="sxs-lookup"><span data-stu-id="22909-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="22909-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="22909-116">Minimum supported client</span></span><br/> | <span data-ttu-id="22909-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22909-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="22909-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="22909-118">Minimum supported server</span></span><br/> | <span data-ttu-id="22909-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22909-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="22909-120">標頭</span><span class="sxs-lookup"><span data-stu-id="22909-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="22909-121"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="22909-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22909-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22909-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22909-123">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="22909-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




