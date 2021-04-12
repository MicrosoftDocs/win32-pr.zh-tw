---
description: 指定中繼資料是否要寫入至轉碼檔案。
ms.assetid: 0fbfc035-c9d1-4014-a28a-93d7e6adc718
title: 'MF_TRANSCODE_SKIP_METADATA_TRANSFER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54978d76ec1392c3be731e1452a653d1423976a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191623"
---
# <a name="mf_transcode_skip_metadata_transfer-attribute"></a><span data-ttu-id="39c8c-103">MF \_ 轉碼 \_ 略過 \_ 中繼資料 \_ 傳輸屬性</span><span class="sxs-lookup"><span data-stu-id="39c8c-103">MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER attribute</span></span>

<span data-ttu-id="39c8c-104">指定中繼資料是否要寫入至轉碼檔案。</span><span class="sxs-lookup"><span data-stu-id="39c8c-104">Specifies whether metadata is written to the transcoded file.</span></span> <span data-ttu-id="39c8c-105">此容器屬性會儲存在轉碼設定檔中。</span><span class="sxs-lookup"><span data-stu-id="39c8c-105">This container attribute is stored in the transcode profile.</span></span>

## <a name="data-type"></a><span data-ttu-id="39c8c-106">資料類型</span><span class="sxs-lookup"><span data-stu-id="39c8c-106">Data type</span></span>

<span data-ttu-id="39c8c-107">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="39c8c-107">**UINT32**</span></span>

<span data-ttu-id="39c8c-108">\_ \_ 下表說明 MF 轉碼略過 \_ 中繼資料 \_ 傳輸屬性的可能值。</span><span class="sxs-lookup"><span data-stu-id="39c8c-108">Possible values for the MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER attribute are described in the following table.</span></span>



| <span data-ttu-id="39c8c-109">值</span><span class="sxs-lookup"><span data-stu-id="39c8c-109">Value</span></span>                                                                        | <span data-ttu-id="39c8c-110">意義</span><span class="sxs-lookup"><span data-stu-id="39c8c-110">Meaning</span></span>                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="39c8c-111"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="39c8c-111"><dt>0</dt></span></span> </dl> | <span data-ttu-id="39c8c-112">自動將檔案層級中繼資料從來源檔案傳送至轉碼檔案。</span><span class="sxs-lookup"><span data-stu-id="39c8c-112">Automatically transfers file-level metadata from the source file to the transcoded file.</span></span><br/> |
| <dl> <span data-ttu-id="39c8c-113"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="39c8c-113"><dt>1</dt></span></span> </dl> | <span data-ttu-id="39c8c-114">來源檔案中繼資料不會寫入至轉碼檔案。</span><span class="sxs-lookup"><span data-stu-id="39c8c-114">The source file metadata is not written to the transcoded file.</span></span><br/>                          |



 

## <a name="getset"></a><span data-ttu-id="39c8c-115">取得/設定</span><span class="sxs-lookup"><span data-stu-id="39c8c-115">Get/set</span></span>

<span data-ttu-id="39c8c-116">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="39c8c-116">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="39c8c-117">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="39c8c-117">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="39c8c-118">備註</span><span class="sxs-lookup"><span data-stu-id="39c8c-118">Remarks</span></span>

<span data-ttu-id="39c8c-119">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="39c8c-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="39c8c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="39c8c-120">Requirements</span></span>



| <span data-ttu-id="39c8c-121">需求</span><span class="sxs-lookup"><span data-stu-id="39c8c-121">Requirement</span></span> | <span data-ttu-id="39c8c-122">值</span><span class="sxs-lookup"><span data-stu-id="39c8c-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="39c8c-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39c8c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="39c8c-124">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39c8c-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="39c8c-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39c8c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="39c8c-126">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39c8c-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="39c8c-127">標頭</span><span class="sxs-lookup"><span data-stu-id="39c8c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="39c8c-128"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="39c8c-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39c8c-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39c8c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c8c-130">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="39c8c-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="39c8c-131">**IMFTranscodeProfile::GetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="39c8c-131">**IMFTranscodeProfile::GetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[<span data-ttu-id="39c8c-132">**IMFTranscodeProfile::SetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="39c8c-132">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




