---
title: FormatCode 登錄專案
description: FormatCode 登錄專案
ms.assetid: cc444eaa-6898-48ab-9573-9e7d5e25d6db
keywords:
- Windows Media Player，FormatCode 登錄專案
- Windows Media Player、副檔名
- Windows Media Player，登錄
- 登錄、副檔名
- 登錄，FormatCode 專案
- 登錄，Windows Media Player 的設定
- 副檔名登錄設定
- FormatCode 登錄專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2318d32e9d7a08a2ae23b24e7acd2674b9eecb2
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104185481"
---
# <a name="formatcode-registry-entry"></a><span data-ttu-id="ba254-111">FormatCode 登錄專案</span><span class="sxs-lookup"><span data-stu-id="ba254-111">FormatCode Registry Entry</span></span>

<span data-ttu-id="ba254-112">當 Windows Media Player 遇到自訂副檔名時，它會尋找符合擴充功能的登錄子機碼。</span><span class="sxs-lookup"><span data-stu-id="ba254-112">When Windows Media Player encounters a custom file name extension, it looks for a registry subkey that matches the extension.</span></span> <span data-ttu-id="ba254-113">此子機碼描述于副檔名登錄 [設定](file-name-extension-registry-settings.md)中。</span><span class="sxs-lookup"><span data-stu-id="ba254-113">The subkey is described in [File Name Extension Registry Settings](file-name-extension-registry-settings.md).</span></span> <span data-ttu-id="ba254-114">其中一個可出現在擴充功能子機碼底下的登錄專案是 **FormatCode** 專案。</span><span class="sxs-lookup"><span data-stu-id="ba254-114">One of the registry entries that can appear under the extension's subkey is the **FormatCode** entry.</span></span>

<span data-ttu-id="ba254-115">**FormatCode** 登錄專案會針對具有自訂延伸模組的檔案，指定 (MTP) 格式代碼的媒體傳輸通訊協定。</span><span class="sxs-lookup"><span data-stu-id="ba254-115">The **FormatCode** registry entry specifies the Media Transport Protocol (MTP) format code for files that have the custom extension.</span></span> <span data-ttu-id="ba254-116">**FormatCode** 登錄專案具有下列格式。</span><span class="sxs-lookup"><span data-stu-id="ba254-116">The **FormatCode** registry entry has the following form.</span></span>



| <span data-ttu-id="ba254-117">名稱</span><span class="sxs-lookup"><span data-stu-id="ba254-117">Name</span></span>       | <span data-ttu-id="ba254-118">類型</span><span class="sxs-lookup"><span data-stu-id="ba254-118">Type</span></span>           | <span data-ttu-id="ba254-119">值</span><span class="sxs-lookup"><span data-stu-id="ba254-119">Value</span></span>                                                             |
|------------|----------------|-------------------------------------------------------------------|
| <span data-ttu-id="ba254-120">FormatCode</span><span class="sxs-lookup"><span data-stu-id="ba254-120">FormatCode</span></span> | <span data-ttu-id="ba254-121">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ba254-121">**REG\_DWORD**</span></span> | <span data-ttu-id="ba254-122">16位的正整數，用來識別檔案的格式。</span><span class="sxs-lookup"><span data-stu-id="ba254-122">A 16-bit positive integer that identifies the format of the file.</span></span> |



 

<span data-ttu-id="ba254-123">當使用者嘗試將副檔名為自訂的數位媒體檔案複製到可攜式裝置時，Windows Media Player 會在登錄中尋找與自訂副檔名相關聯的格式代碼。</span><span class="sxs-lookup"><span data-stu-id="ba254-123">When the user attempts to copy a digital media file that has a custom file name extension to a portable device, Windows Media Player looks in the registry to find a format code associated with the custom file name extension.</span></span> <span data-ttu-id="ba254-124">如果 Windows Media Player 找到格式代碼，則會使用 MTP 來判斷裝置是否支援自訂檔案格式。</span><span class="sxs-lookup"><span data-stu-id="ba254-124">If Windows Media Player finds a format code, it uses MTP to determine whether the device supports the custom file format.</span></span> <span data-ttu-id="ba254-125">如果裝置支援此格式，則會將媒體檔案複製到裝置上，而不會轉碼。</span><span class="sxs-lookup"><span data-stu-id="ba254-125">If the device supports the format, the media file is copied to the device without being transcoded.</span></span>

<span data-ttu-id="ba254-126">支援 MTP 的裝置可以提供 DeviceInfo 資料集 Windows Media Player，其中包含裝置所支援的格式代碼清單，還有其他專案。</span><span class="sxs-lookup"><span data-stu-id="ba254-126">A device that supports MTP can supply Windows Media Player with a DeviceInfo dataset, which contains, among other things, a list of format codes supported by the device.</span></span>

<span data-ttu-id="ba254-127">如果您正在開發自訂檔案格式，您可以向 Microsoft 要求格式代碼。</span><span class="sxs-lookup"><span data-stu-id="ba254-127">If you are in the process of developing a custom file format, you can request a format code from Microsoft.</span></span> <span data-ttu-id="ba254-128">如需有關如何要求格式代碼的詳細資訊，請參閱 microsoft [Windows Media 開發人員中心](https://msdn.microsoft.com/windowsmedia/default.aspx)提供的 Microsoft 媒體傳輸通訊協定移植套件。</span><span class="sxs-lookup"><span data-stu-id="ba254-128">For information about how to request a format code, see the Microsoft Media Transport Protocol Porting Kit, which is available at the [Microsoft Windows Media Developer Center](https://msdn.microsoft.com/windowsmedia/default.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba254-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="ba254-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba254-130">**副檔名登錄設定**</span><span class="sxs-lookup"><span data-stu-id="ba254-130">**File Name Extension Registry Settings**</span></span>](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




