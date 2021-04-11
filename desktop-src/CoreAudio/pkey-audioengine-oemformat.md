---
description: PKEY \_ AudioEngine \_ OEMFormat 屬性會指定用來轉譯或捕捉資料流程之裝置的預設格式。 在 .inf 檔案中，OEM 會填入這些值。
ms.assetid: 3a199ecf-642c-491c-a565-f0083783d180
title: 'PKEY_AudioEngine_OEMFormat (Mmdeviceapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7ed65ae8a7bd717992b13dc7b5517a5725b241
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111312"
---
# <a name="pkey_audioengine_oemformat"></a><span data-ttu-id="9571d-104">PKEY \_ AudioEngine \_ OEMFormat</span><span class="sxs-lookup"><span data-stu-id="9571d-104">PKEY\_AudioEngine\_OEMFormat</span></span>

<span data-ttu-id="9571d-105">PKEY \_ AudioEngine \_ OEMFormat 屬性會指定用來轉譯或捕捉資料流程之裝置的預設格式。</span><span class="sxs-lookup"><span data-stu-id="9571d-105">The PKEY\_AudioEngine\_OEMFormat property specifies the default format of the device that is used for rendering or capturing a stream.</span></span> <span data-ttu-id="9571d-106">在 .inf 檔案中，OEM 會填入這些值。</span><span class="sxs-lookup"><span data-stu-id="9571d-106">The values are populated by the OEM in an .inf file.</span></span>

<span data-ttu-id="9571d-107">**PROPVARIANT** 結構的 **vt** 成員會設定為 vt \_ BLOB。</span><span class="sxs-lookup"><span data-stu-id="9571d-107">The **vt** member of the **PROPVARIANT** structure is set to VT\_BLOB.</span></span>

<span data-ttu-id="9571d-108">**PROPVARIANT** 結構的 **Blob** 成員是 **blob** 類型的結構，其中包含兩個成員。</span><span class="sxs-lookup"><span data-stu-id="9571d-108">The **blob** member of the **PROPVARIANT** structure is a structure of type **BLOB** that contains two members.</span></span> <span data-ttu-id="9571d-109">成員 **blob。 cbSize** 是一個 **DWORD** ，可指定格式描述中的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="9571d-109">Member **blob.cbSize** is a **DWORD** that specifies the number of bytes in the format description.</span></span> <span data-ttu-id="9571d-110">成員 **blob. pBlobData** 指向包含格式描述的 **WAVEFORMATEX** 結構。</span><span class="sxs-lookup"><span data-stu-id="9571d-110">Member **blob.pBlobData** points to a **WAVEFORMATEX** structure that contains the format description.</span></span> <span data-ttu-id="9571d-111">如需 BLOB 的詳細資訊，請參閱 Windows SDK 檔。</span><span class="sxs-lookup"><span data-stu-id="9571d-111">For more information about BLOB, see the Windows SDK documentation.</span></span> <span data-ttu-id="9571d-112">如需 **WAVEFORMATEX** 的詳細資訊，請參閱 Windows DDK 檔。</span><span class="sxs-lookup"><span data-stu-id="9571d-112">For more information about **WAVEFORMATEX**, see the Windows DDK documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="9571d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9571d-113">Requirements</span></span>



| <span data-ttu-id="9571d-114">需求</span><span class="sxs-lookup"><span data-stu-id="9571d-114">Requirement</span></span> | <span data-ttu-id="9571d-115">值</span><span class="sxs-lookup"><span data-stu-id="9571d-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9571d-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9571d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9571d-117">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9571d-117">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9571d-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9571d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9571d-119">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9571d-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9571d-120">標頭</span><span class="sxs-lookup"><span data-stu-id="9571d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9571d-121"><dt>Mmdeviceapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="9571d-121"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9571d-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9571d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9571d-123">**音訊端點屬性**</span><span class="sxs-lookup"><span data-stu-id="9571d-123">**Audio Endpoint Properties**</span></span>](audio-endpoint-properties.md)
</dt> <dt>

[<span data-ttu-id="9571d-124">核心音訊屬性</span><span class="sxs-lookup"><span data-stu-id="9571d-124">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> </dl>

 

 




