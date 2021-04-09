---
description: 指定媒體基礎轉換 (MFT) 應該如何輸出 3D stereoscopic 影片串流。
ms.assetid: AA75A2FB-DEAC-44E9-93E9-4AC2D9F03B39
title: 'MF_ENABLE_3DVIDEO_OUTPUT 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0123a574ec74ed4aa9fa0aea3b2cabecbb29da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848527"
---
# <a name="mf_enable_3dvideo_output-attribute"></a><span data-ttu-id="d7a70-103">MF \_ 啟用 \_ 3DVIDEO \_ 輸出屬性</span><span class="sxs-lookup"><span data-stu-id="d7a70-103">MF\_ENABLE\_3DVIDEO\_OUTPUT attribute</span></span>

<span data-ttu-id="d7a70-104">指定媒體基礎轉換 (MFT) 應該如何輸出 3D stereoscopic 影片串流。</span><span class="sxs-lookup"><span data-stu-id="d7a70-104">Specifies how a Media Foundation transform (MFT) should output a 3D stereoscopic video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="d7a70-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="d7a70-105">Data type</span></span>

<span data-ttu-id="d7a70-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d7a70-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d7a70-107">備註</span><span class="sxs-lookup"><span data-stu-id="d7a70-107">Remarks</span></span>

<span data-ttu-id="d7a70-108">屬性的值是 [**MF3DVideoOutputType**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype) 列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="d7a70-108">The value of the attribute is a member of the [**MF3DVideoOutputType**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype) enumeration.</span></span>

<span data-ttu-id="d7a70-109">只有當 MFT [ \_ 支援 \_ 3DVIDEO](mft-support-3dvideo.md)屬性的 **值為 TRUE** 時，才會套用此屬性。</span><span class="sxs-lookup"><span data-stu-id="d7a70-109">This attribute applies only if the MFT returns **TRUE** for the [MFT\_SUPPORT\_3DVIDEO](mft-support-3dvideo.md) attribute.</span></span>

<span data-ttu-id="d7a70-110">若要取得或設定此屬性，請呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 來取得 MFT 的全域屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="d7a70-110">To get or set this attribute call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store of the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7a70-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7a70-111">Requirements</span></span>



| <span data-ttu-id="d7a70-112">需求</span><span class="sxs-lookup"><span data-stu-id="d7a70-112">Requirement</span></span> | <span data-ttu-id="d7a70-113">值</span><span class="sxs-lookup"><span data-stu-id="d7a70-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7a70-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7a70-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d7a70-115">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7a70-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="d7a70-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7a70-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d7a70-117">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7a70-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="d7a70-118">標頭</span><span class="sxs-lookup"><span data-stu-id="d7a70-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7a70-119"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="d7a70-119"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7a70-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7a70-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7a70-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="d7a70-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




