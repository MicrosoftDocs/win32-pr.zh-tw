---
description: 指定硬體裝置來源是否使用時間戳的系統時間。
ms.assetid: 54cdfa13-955a-4e92-b337-f645d526a1b8
title: 'MFT_HW_TIMESTAMP_WITH_QPC_Attribute 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94f6f7d50db89e99e76e7b7ea509f444c3998bb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986854"
---
# <a name="mft_hw_timestamp_with_qpc_attribute-attribute"></a><span data-ttu-id="65b85-103">\_ \_ \_ 具有 \_ QPC \_ 屬性屬性的 MFT HW TIMESTAMP</span><span class="sxs-lookup"><span data-stu-id="65b85-103">MFT\_HW\_TIMESTAMP\_WITH\_QPC\_Attribute attribute</span></span>

<span data-ttu-id="65b85-104">指定硬體裝置來源是否使用時間戳的系統時間。</span><span class="sxs-lookup"><span data-stu-id="65b85-104">Specifies whether a hardware device source uses the system time for time stamps.</span></span>

## <a name="data-type"></a><span data-ttu-id="65b85-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="65b85-105">Data type</span></span>

<span data-ttu-id="65b85-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="65b85-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="65b85-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="65b85-107">Get/set</span></span>

<span data-ttu-id="65b85-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="65b85-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="65b85-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="65b85-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="65b85-110">備註</span><span class="sxs-lookup"><span data-stu-id="65b85-110">Remarks</span></span>

<span data-ttu-id="65b85-111">如果此屬性為 **TRUE**，則裝置來源會使用 **QueryPerformanceCounter** 所傳回的系統時間來表示時間戳記。</span><span class="sxs-lookup"><span data-stu-id="65b85-111">If this attribute is **TRUE**, the device source uses the system time, as returned by the **QueryPerformanceCounter**, for time stamps.</span></span> <span data-ttu-id="65b85-112">否則，裝置來源會使用裝置的時鐘。</span><span class="sxs-lookup"><span data-stu-id="65b85-112">Otherwise, the device source uses the device's clock.</span></span> <span data-ttu-id="65b85-113">預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="65b85-113">The default value is **FALSE**.</span></span>

<span data-ttu-id="65b85-114">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="65b85-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="65b85-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="65b85-115">Requirements</span></span>



| <span data-ttu-id="65b85-116">需求</span><span class="sxs-lookup"><span data-stu-id="65b85-116">Requirement</span></span> | <span data-ttu-id="65b85-117">值</span><span class="sxs-lookup"><span data-stu-id="65b85-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="65b85-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65b85-118">Minimum supported client</span></span><br/> | <span data-ttu-id="65b85-119">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65b85-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="65b85-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65b85-120">Minimum supported server</span></span><br/> | <span data-ttu-id="65b85-121">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65b85-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="65b85-122">標頭</span><span class="sxs-lookup"><span data-stu-id="65b85-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="65b85-123"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="65b85-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65b85-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65b85-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b85-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="65b85-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="65b85-126">捕獲裝置屬性</span><span class="sxs-lookup"><span data-stu-id="65b85-126">Capture Device Attributes</span></span>](capture-device-attributes.md)
</dt> </dl>

 

 




