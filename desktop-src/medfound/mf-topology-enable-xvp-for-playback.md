---
description: 指定拓撲載入器是否會啟用轉碼視頻處理器 (XVP) 。 針對轉換，啟用硬體加速色彩轉換。
title: 'MF_TOPOLOGY_ENABLE_XVP_FOR_PLAYBACK 屬性 (Mfidl) '
ms.topic: reference
ms.date: 02/22/2021
ms.openlocfilehash: e36841db57e8343248ef5e369915d4bc357815bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106981972"
---
# <a name="mf_topology_enable_xvp_for_playback-attribute"></a><span data-ttu-id="17950-104">MF \_ 拓撲 \_ 啟用 \_ XVP \_ 的 \_ 播放屬性</span><span class="sxs-lookup"><span data-stu-id="17950-104">MF\_TOPOLOGY\_ENABLE\_XVP\_FOR\_PLAYBACK attribute</span></span>

<span data-ttu-id="17950-105">指定拓撲載入器是否會啟用轉碼視頻處理器 (XVP) 。</span><span class="sxs-lookup"><span data-stu-id="17950-105">Specifies whether the topology loader enables the Transcode Video Processor (XVP).</span></span> <span data-ttu-id="17950-106">針對轉換，啟用硬體加速色彩轉換。</span><span class="sxs-lookup"><span data-stu-id="17950-106">for conversions, enabling hardware accelerated color conversion.</span></span>

## <a name="data-type"></a><span data-ttu-id="17950-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="17950-107">Data type</span></span>

<span data-ttu-id="17950-108">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="17950-108">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="17950-109">取得/設定</span><span class="sxs-lookup"><span data-stu-id="17950-109">Get/set</span></span>

<span data-ttu-id="17950-110">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="17950-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="17950-111">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="17950-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="17950-112">適用於</span><span class="sxs-lookup"><span data-stu-id="17950-112">Applies to</span></span>

[<span data-ttu-id="17950-113">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="17950-113">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="17950-114">備註</span><span class="sxs-lookup"><span data-stu-id="17950-114">Remarks</span></span>

<span data-ttu-id="17950-115">如果設定此屬性，拓撲載入器會在非轉碼拓撲解析期間，于必要時，提取視頻處理器。</span><span class="sxs-lookup"><span data-stu-id="17950-115">If this attribute is set, the topology loader will pull in the video processor, if necessary, during non-transcode topology resolution.</span></span> <span data-ttu-id="17950-116">當您使用拓撲來建立自己的 [IMFTopology](/windows/win32/api/mfidl/nn-mfidl-imftopology) 時，此屬性會告知載入器使用 XVP 進行轉換，而不是使用舊版色彩轉換器，進而啟用硬體加速色彩轉換;舊版色彩轉換器僅限軟體。</span><span class="sxs-lookup"><span data-stu-id="17950-116">When you are using the topology to build your own [IMFTopology](/windows/win32/api/mfidl/nn-mfidl-imftopology) this attribute tells the loader to use XVP for conversions instead of the legacy color converter, thus enabling hardware accelerated color conversion; the legacy color converter is software-only.</span></span>

## <a name="requirements"></a><span data-ttu-id="17950-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="17950-117">Requirements</span></span>



| <span data-ttu-id="17950-118">需求</span><span class="sxs-lookup"><span data-stu-id="17950-118">Requirement</span></span> | <span data-ttu-id="17950-119">值</span><span class="sxs-lookup"><span data-stu-id="17950-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="17950-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17950-120">Minimum supported client</span></span><br/> | <span data-ttu-id="17950-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17950-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="17950-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17950-122">Minimum supported server</span></span><br/> | <span data-ttu-id="17950-123">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="17950-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="17950-124">標頭</span><span class="sxs-lookup"><span data-stu-id="17950-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="17950-125"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="17950-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17950-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17950-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17950-127">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="17950-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="17950-128">Direct3D 裝置管理員</span><span class="sxs-lookup"><span data-stu-id="17950-128">Direct3D Device Manager</span></span>](direct3d-device-manager.md)
</dt> <dt>

[<span data-ttu-id="17950-129">拓撲屬性</span><span class="sxs-lookup"><span data-stu-id="17950-129">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




