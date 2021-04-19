---
description: 包含媒體基礎轉換 (MFT) 的已註冊輸出類型。
ms.assetid: 925267a2-4421-4874-a8a2-437876c729f1
title: 'MFT_OUTPUT_TYPES_Attributes 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 991b94b52782eb631846ee1ce182b4676a3cfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973708"
---
# <a name="mft_output_types_attributes-attribute"></a><span data-ttu-id="537a8-103">MFT \_ 輸出 \_ 類型 \_ 屬性屬性</span><span class="sxs-lookup"><span data-stu-id="537a8-103">MFT\_OUTPUT\_TYPES\_Attributes attribute</span></span>

<span data-ttu-id="537a8-104">包含媒體基礎轉換 (MFT) 的已註冊輸出類型。</span><span class="sxs-lookup"><span data-stu-id="537a8-104">Contains the registered output types for a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="537a8-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="537a8-105">Data type</span></span>

<span data-ttu-id="537a8-106">**MFT \_儲存 \_ 為 \_ \[ \]** **位元組 \[ 的註冊類型 \]** 資訊</span><span class="sxs-lookup"><span data-stu-id="537a8-106">**MFT\_REGISTER\_TYPE\_INFO\[\]** stored as **BYTE\[\]**</span></span>

## <a name="remarks"></a><span data-ttu-id="537a8-107">備註</span><span class="sxs-lookup"><span data-stu-id="537a8-107">Remarks</span></span>

<span data-ttu-id="537a8-108">這個屬性是在 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)函數所傳回的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標上設定的。</span><span class="sxs-lookup"><span data-stu-id="537a8-108">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="537a8-109">此屬性包含 [**mft 登錄 \_ \_ 類型 \_ 資訊**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) 結構的陣列，其描述 mft 所支援的一或多個輸出格式。</span><span class="sxs-lookup"><span data-stu-id="537a8-109">This attribute contains an array of [**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) structures that describe one or more output formats supported by the MFT.</span></span> <span data-ttu-id="537a8-110">這些值會從登錄中取得，並作為應用程式的提示。</span><span class="sxs-lookup"><span data-stu-id="537a8-110">These values are taken from the registry and are intended as a hint to the application.</span></span> <span data-ttu-id="537a8-111">MFT 可能會支援其他格式。</span><span class="sxs-lookup"><span data-stu-id="537a8-111">The MFT might support additional formats.</span></span> <span data-ttu-id="537a8-112">若要設定實際的輸出格式，您必須建立 MFT 並呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)。</span><span class="sxs-lookup"><span data-stu-id="537a8-112">To set the actual output format, you must create the MFT and call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

<span data-ttu-id="537a8-113">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="537a8-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="537a8-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="537a8-114">Requirements</span></span>



| <span data-ttu-id="537a8-115">需求</span><span class="sxs-lookup"><span data-stu-id="537a8-115">Requirement</span></span> | <span data-ttu-id="537a8-116">值</span><span class="sxs-lookup"><span data-stu-id="537a8-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="537a8-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="537a8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="537a8-118">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="537a8-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="537a8-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="537a8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="537a8-120">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="537a8-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="537a8-121">標頭</span><span class="sxs-lookup"><span data-stu-id="537a8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="537a8-122"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="537a8-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="537a8-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="537a8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="537a8-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="537a8-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="537a8-125">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="537a8-125">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




