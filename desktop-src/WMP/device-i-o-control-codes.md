---
title: 裝置 i/o 控制碼
description: 裝置 i/o 控制碼
ms.assetid: 46a5d166-ca8d-42df-9455-145332437153
keywords:
- Windows Media Player、裝置 i/o 控制碼
- Windows Media Player，控制代碼
- Windows Media 裝置管理員
- 裝置 i/o 控制碼
- 控制代碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69c00e235ce0f0e68e98f4f0e37221eac0903682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965992"
---
# <a name="device-io-control-codes"></a><span data-ttu-id="4bf4a-108">裝置 i/o 控制碼</span><span class="sxs-lookup"><span data-stu-id="4bf4a-108">Device I/O Control Codes</span></span>

<span data-ttu-id="4bf4a-109">Windows Media Player 10 或更新版本會定義 Windows Media 裝置管理員裝置 i/o 控制碼。</span><span class="sxs-lookup"><span data-stu-id="4bf4a-109">Windows Media Player 10 or later defines Windows Media Device Manager device I/O control codes.</span></span> <span data-ttu-id="4bf4a-110">下表包含控制碼及其描述。</span><span class="sxs-lookup"><span data-stu-id="4bf4a-110">The following table contains the control codes and their descriptions.</span></span>



| <span data-ttu-id="4bf4a-111">I/o 控制項程式碼</span><span class="sxs-lookup"><span data-stu-id="4bf4a-111">I/O control code</span></span>                      | <span data-ttu-id="4bf4a-112">值</span><span class="sxs-lookup"><span data-stu-id="4bf4a-112">Value</span></span>      | <span data-ttu-id="4bf4a-113">描述</span><span class="sxs-lookup"><span data-stu-id="4bf4a-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bf4a-114">**IOCTL \_ WMP \_ 中繼資料 \_ 來回 \_ 行程**</span><span class="sxs-lookup"><span data-stu-id="4bf4a-114">**IOCTL\_WMP\_METADATA\_ROUND\_TRIP**</span></span> | <span data-ttu-id="4bf4a-115">0x31504d57</span><span class="sxs-lookup"><span data-stu-id="4bf4a-115">0x31504d57</span></span> | <span data-ttu-id="4bf4a-116">管理有關中繼資料值發生之變更的資訊傳輸。</span><span class="sxs-lookup"><span data-stu-id="4bf4a-116">Manages transfer of information about changes that occurred to metadata values.</span></span> <span data-ttu-id="4bf4a-117">請參閱 [用於加速中繼資料傳輸的裝置延伸](device-extensions-for-accelerated-metadata-transfer.md)模組。</span><span class="sxs-lookup"><span data-stu-id="4bf4a-117">See [Device Extensions for Accelerated Metadata Transfer](device-extensions-for-accelerated-metadata-transfer.md).</span></span>                                                                                                                                                                          |
| <span data-ttu-id="4bf4a-118">**IOCTL \_ WMP \_ 裝置 \_ 可 \_ 同步**</span><span class="sxs-lookup"><span data-stu-id="4bf4a-118">**IOCTL\_WMP\_DEVICE\_CAN\_SYNC**</span></span>     | <span data-ttu-id="4bf4a-119">0x32504d57</span><span class="sxs-lookup"><span data-stu-id="4bf4a-119">0x32504d57</span></span> | <span data-ttu-id="4bf4a-120">指出可攜式裝置是否支援自動同步處理。</span><span class="sxs-lookup"><span data-stu-id="4bf4a-120">Indicates whether a portable device supports automatic synchronization.</span></span> <span data-ttu-id="4bf4a-121">Windows Media Player 10 或更新版本不會提供任何輸入緩衝區。輸出緩衝區必須傳回 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="4bf4a-121">Windows Media Player 10 or later provides no input buffer.The output buffer must return a **DWORD** value.</span></span> <span data-ttu-id="4bf4a-122">1值表示裝置支援同步處理。</span><span class="sxs-lookup"><span data-stu-id="4bf4a-122">A value of 1 means the device supports synchronization.</span></span> <span data-ttu-id="4bf4a-123">值為0表示裝置不支援自動同步處理。</span><span class="sxs-lookup"><span data-stu-id="4bf4a-123">A value of 0 means the device does not support automatic synchronization.</span></span><br/> <span data-ttu-id="4bf4a-124">如需詳細資訊，請參閱「備註」。</span><span class="sxs-lookup"><span data-stu-id="4bf4a-124">See Remarks for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4bf4a-125">備註</span><span class="sxs-lookup"><span data-stu-id="4bf4a-125">Remarks</span></span>

<span data-ttu-id="4bf4a-126">這些控制項代碼定義于 wmpdevices 中。</span><span class="sxs-lookup"><span data-stu-id="4bf4a-126">These control codes are defined in wmpdevices.h.</span></span>

<span data-ttu-id="4bf4a-127">如果裝置不支援 **\_ \_ \_ 可 \_ 同步的 IOCTL WMP 裝置**，Windows Media Player 10 或更新版本會假設裝置支援自動同步處理。</span><span class="sxs-lookup"><span data-stu-id="4bf4a-127">If the device does not support **IOCTL\_WMP\_DEVICE\_CAN\_SYNC**, Windows Media Player 10 or later assumes the device supports automatic synchronization.</span></span> <span data-ttu-id="4bf4a-128">請注意，雖然這個值可能不允許自動同步處理，但是還有其他準則用來判斷裝置是否支援自動同步處理。</span><span class="sxs-lookup"><span data-stu-id="4bf4a-128">Note that while this value can disallow automatic synchronization, there are additional criteria used to determine whether the device supports automatic synchronization.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4bf4a-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="4bf4a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bf4a-130">**加速中繼資料傳輸的裝置擴充功能**</span><span class="sxs-lookup"><span data-stu-id="4bf4a-130">**Device Extensions for Accelerated Metadata Transfer**</span></span>](device-extensions-for-accelerated-metadata-transfer.md)
</dt> <dt>

[<span data-ttu-id="4bf4a-131">**Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="4bf4a-131">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 





