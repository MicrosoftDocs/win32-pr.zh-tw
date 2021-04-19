---
description: 磁帶位置搜尋
ms.assetid: 17fb4eba-4b2c-41c2-94e2-e58586f92e53
title: 磁帶位置搜尋
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33d1fb719f3b43374e5aa86f34c60e5b8f14d536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980601"
---
# <a name="tape-location-search"></a><span data-ttu-id="adbd4-103">磁帶位置搜尋</span><span class="sxs-lookup"><span data-stu-id="adbd4-103">Tape Location Search</span></span>

<span data-ttu-id="adbd4-104">雖然 DV 裝置支援依時間碼或 (ATN) 的絕對軌編號來搜尋的命令，但是 MSDV 驅動程式並沒有可存取這些函式的標準、與裝置無關的方式。</span><span class="sxs-lookup"><span data-stu-id="adbd4-104">Although DV devices support a command to search by time code or by absolute track number (ATN), the MSDV driver does not have a standard, device-independent way to access these functions.</span></span> <span data-ttu-id="adbd4-105">唯一的選項是將未經處理的 AV/C 命令傳送到驅動程式，如 [發出原始的 av/c 命令](issuing-raw-av-c-commands.md)所述。</span><span class="sxs-lookup"><span data-stu-id="adbd4-105">The only option is to send a raw AV/C command to the driver as described in the topic [Issuing Raw AV/C Commands](issuing-raw-av-c-commands.md).</span></span>

<span data-ttu-id="adbd4-106">UVC 驅動程式支援磁帶位置搜尋的屬性集。</span><span class="sxs-lookup"><span data-stu-id="adbd4-106">The UVC driver supports a property set for tape location searches.</span></span> <span data-ttu-id="adbd4-107">若要傳送搜尋命令，請使用 **IKsControl** 介面並設定 PROPSETID \_ EXT \_ TRANSPORT 屬性。</span><span class="sxs-lookup"><span data-stu-id="adbd4-107">To send a search command, use the **IKsControl** interface and set the PROPSETID\_EXT\_TRANSPORT property.</span></span> <span data-ttu-id="adbd4-108">使用屬性集比將未經處理的 AV/C 命令傳送到裝置更安全，因為 AV/C 命令會略過篩選器並直接移至設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="adbd4-108">Using a property set is safer than sending raw AV/C commands to the device, because AV/C commands bypass the filter and go directly to the device driver.</span></span>

## <a name="related-topics"></a><span data-ttu-id="adbd4-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="adbd4-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adbd4-110">控制 DV 攝像機</span><span class="sxs-lookup"><span data-stu-id="adbd4-110">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> <dt>

[<span data-ttu-id="adbd4-111">外部裝置傳輸屬性集</span><span class="sxs-lookup"><span data-stu-id="adbd4-111">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



