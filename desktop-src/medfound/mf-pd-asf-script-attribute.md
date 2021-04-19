---
description: 指定指令碼命令清單以及 Advanced 系統格式的參數 (ASF) 檔。 這個屬性會對應到 ASF 規格中定義的 ASF 標頭中的指令碼命令物件。
ms.assetid: c85c9da4-f0b5-4055-a645-2a71cabbe4a3
title: 'MF_PD_ASF_SCRIPT 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03de86298d28183aa57cc80b451c4e46bb054de2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987236"
---
# <a name="mf_pd_asf_script-attribute"></a><span data-ttu-id="1af9d-104">MF \_ PD \_ ASF \_ 腳本屬性</span><span class="sxs-lookup"><span data-stu-id="1af9d-104">MF\_PD\_ASF\_SCRIPT attribute</span></span>

<span data-ttu-id="1af9d-105">指定指令碼命令清單以及 Advanced 系統格式的參數 (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="1af9d-105">Specifies a list of script commands and the parameters for an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="1af9d-106">這個屬性會對應到 ASF 規格中定義的 ASF 標頭中的指令碼命令物件。</span><span class="sxs-lookup"><span data-stu-id="1af9d-106">This attribute corresponds to the Script Command Object in the ASF header, defined in the ASF specification.</span></span>

## <a name="data-type"></a><span data-ttu-id="1af9d-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="1af9d-107">Data type</span></span>

<span data-ttu-id="1af9d-108">位元組陣列</span><span class="sxs-lookup"><span data-stu-id="1af9d-108">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="1af9d-109">備註</span><span class="sxs-lookup"><span data-stu-id="1af9d-109">Remarks</span></span>

<span data-ttu-id="1af9d-110">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="1af9d-110">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="1af9d-111">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會建立展示描述項，並從指令碼命令物件標頭產生此屬性。</span><span class="sxs-lookup"><span data-stu-id="1af9d-111">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method creates the presentation descriptor and generates this attribute from the Script Command Object header.</span></span> <span data-ttu-id="1af9d-112">下表顯示 blob 的格式：</span><span class="sxs-lookup"><span data-stu-id="1af9d-112">The following table shows the format of the blob:</span></span>



| <span data-ttu-id="1af9d-113">指令碼命令物件欄位</span><span class="sxs-lookup"><span data-stu-id="1af9d-113">Script Command Object field</span></span> | <span data-ttu-id="1af9d-114">資料類型</span><span class="sxs-lookup"><span data-stu-id="1af9d-114">Data type</span></span>    | <span data-ttu-id="1af9d-115">大小</span><span class="sxs-lookup"><span data-stu-id="1af9d-115">Size</span></span>    | <span data-ttu-id="1af9d-116">Description</span><span class="sxs-lookup"><span data-stu-id="1af9d-116">Description</span></span>               |
|-----------------------------|--------------|---------|---------------------------|
| <span data-ttu-id="1af9d-117">命令計數</span><span class="sxs-lookup"><span data-stu-id="1af9d-117">Commands Count</span></span>              | <span data-ttu-id="1af9d-118">**Dword**</span><span class="sxs-lookup"><span data-stu-id="1af9d-118">**DWORD**</span></span>    | <span data-ttu-id="1af9d-119">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="1af9d-119">4 bytes</span></span> | <span data-ttu-id="1af9d-120">指令碼命令數目</span><span class="sxs-lookup"><span data-stu-id="1af9d-120">Number of script commands</span></span> |
| <span data-ttu-id="1af9d-121">命令類型，命令</span><span class="sxs-lookup"><span data-stu-id="1af9d-121">Command Type, Commands</span></span>      | <span data-ttu-id="1af9d-122">**位元組**\[\]</span><span class="sxs-lookup"><span data-stu-id="1af9d-122">**BYTE**\[\]</span></span> | <span data-ttu-id="1af9d-123">不定</span><span class="sxs-lookup"><span data-stu-id="1af9d-123">Varies</span></span>  | <span data-ttu-id="1af9d-124">指令碼命令陣列</span><span class="sxs-lookup"><span data-stu-id="1af9d-124">Array of script commands</span></span>  |



 

<span data-ttu-id="1af9d-125">第一個 **DWORD** 是指令碼命令的數目，後面接著命令陣列。</span><span class="sxs-lookup"><span data-stu-id="1af9d-125">The first **DWORD** is the number of script commands, followed by an array of commands.</span></span> <span data-ttu-id="1af9d-126">每個指令碼命令都具有下列格式：</span><span class="sxs-lookup"><span data-stu-id="1af9d-126">Each script command has the following format:</span></span>



| <span data-ttu-id="1af9d-127">指令碼命令物件欄位</span><span class="sxs-lookup"><span data-stu-id="1af9d-127">Script Command Object field</span></span> | <span data-ttu-id="1af9d-128">資料類型</span><span class="sxs-lookup"><span data-stu-id="1af9d-128">Data type</span></span>     | <span data-ttu-id="1af9d-129">大小</span><span class="sxs-lookup"><span data-stu-id="1af9d-129">Size</span></span>    | <span data-ttu-id="1af9d-130">Description</span><span class="sxs-lookup"><span data-stu-id="1af9d-130">Description</span></span>                                                              |
|-----------------------------|---------------|---------|--------------------------------------------------------------------------|
| <span data-ttu-id="1af9d-131">命令名稱長度</span><span class="sxs-lookup"><span data-stu-id="1af9d-131">Command Name Length</span></span>         | <span data-ttu-id="1af9d-132">**Dword**</span><span class="sxs-lookup"><span data-stu-id="1af9d-132">**DWORD**</span></span>     | <span data-ttu-id="1af9d-133">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="1af9d-133">4 bytes</span></span> | <span data-ttu-id="1af9d-134">命令字串的大小（以位元組為單位），包括 Null 字元。</span><span class="sxs-lookup"><span data-stu-id="1af9d-134">Size of the command string, in bytes, including the NULL character.</span></span>      |
| <span data-ttu-id="1af9d-135">命令名稱：</span><span class="sxs-lookup"><span data-stu-id="1af9d-135">Command Name</span></span>                | <span data-ttu-id="1af9d-136">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="1af9d-136">**WCHAR**\[\]</span></span> | <span data-ttu-id="1af9d-137">不定</span><span class="sxs-lookup"><span data-stu-id="1af9d-137">Varies</span></span>  | <span data-ttu-id="1af9d-138">以 Null 終止的字串，其中包含指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="1af9d-138">Null-terminated string that contains the script command.</span></span>                 |
| <span data-ttu-id="1af9d-139">命令類型名稱長度</span><span class="sxs-lookup"><span data-stu-id="1af9d-139">Command Type Name Length</span></span>    | <span data-ttu-id="1af9d-140">**Dword**</span><span class="sxs-lookup"><span data-stu-id="1af9d-140">**DWORD**</span></span>     | <span data-ttu-id="1af9d-141">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="1af9d-141">4 bytes</span></span> | <span data-ttu-id="1af9d-142">命令類型字串的大小（以位元組為單位），包括 Null 字元。</span><span class="sxs-lookup"><span data-stu-id="1af9d-142">Size of the command type string, in bytes, including the NULL character.</span></span> |
| <span data-ttu-id="1af9d-143">命令類型名稱</span><span class="sxs-lookup"><span data-stu-id="1af9d-143">Command Type Name</span></span>           | <span data-ttu-id="1af9d-144">**WCHAR**\[\]</span><span class="sxs-lookup"><span data-stu-id="1af9d-144">**WCHAR**\[\]</span></span> | <span data-ttu-id="1af9d-145">不定</span><span class="sxs-lookup"><span data-stu-id="1af9d-145">Varies</span></span>  | <span data-ttu-id="1af9d-146">以 Null 終止的字串，其中包含命令類型。</span><span class="sxs-lookup"><span data-stu-id="1af9d-146">Null-terminated string that contains the command type.</span></span>                   |
| <span data-ttu-id="1af9d-147">呈現時間</span><span class="sxs-lookup"><span data-stu-id="1af9d-147">Presentation Time</span></span>           | <span data-ttu-id="1af9d-148">**Dword**</span><span class="sxs-lookup"><span data-stu-id="1af9d-148">**DWORD**</span></span>     | <span data-ttu-id="1af9d-149">4 個位元組</span><span class="sxs-lookup"><span data-stu-id="1af9d-149">4 bytes</span></span> | <span data-ttu-id="1af9d-150">命令的呈現時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="1af9d-150">Presentation time of the command in milliseconds.</span></span>                        |



 

## <a name="requirements"></a><span data-ttu-id="1af9d-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="1af9d-151">Requirements</span></span>



| <span data-ttu-id="1af9d-152">需求</span><span class="sxs-lookup"><span data-stu-id="1af9d-152">Requirement</span></span> | <span data-ttu-id="1af9d-153">值</span><span class="sxs-lookup"><span data-stu-id="1af9d-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1af9d-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1af9d-154">Minimum supported client</span></span><br/> | <span data-ttu-id="1af9d-155">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1af9d-155">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1af9d-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1af9d-156">Minimum supported server</span></span><br/> | <span data-ttu-id="1af9d-157">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1af9d-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1af9d-158">標頭</span><span class="sxs-lookup"><span data-stu-id="1af9d-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="1af9d-159"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="1af9d-159"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1af9d-160">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1af9d-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1af9d-161">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="1af9d-161">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1af9d-162">**IMFAttributes：： GetBlob**</span><span class="sxs-lookup"><span data-stu-id="1af9d-162">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="1af9d-163">**IMFAttributes：： SetBlob**</span><span class="sxs-lookup"><span data-stu-id="1af9d-163">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="1af9d-164">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="1af9d-164">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="1af9d-165">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="1af9d-165">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="1af9d-166">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="1af9d-166">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="1af9d-167">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="1af9d-167">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




