---
description: 後續的 DVD 區域變更
ms.assetid: 08c0b48a-2851-40c8-addc-21baeb83df1b
title: 後續的 DVD 區域變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78a28982d6807fa5d90356d15cbf5365a595c293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987362"
---
# <a name="subsequent-dvd-region-change"></a><span data-ttu-id="af9ea-103">後續的 DVD 區域變更</span><span class="sxs-lookup"><span data-stu-id="af9ea-103">Subsequent DVD Region Change</span></span>

<span data-ttu-id="af9ea-104">在 Windows 2000 和更新版本中，DVD 導覽器會在裝置管理員的 DVD-ROM 光碟機裝置上叫用屬性頁。</span><span class="sxs-lookup"><span data-stu-id="af9ea-104">In Windows 2000 and later, the DVD Navigator invokes a property page on the DVD-ROM drive device in the Device Manager.</span></span> <span data-ttu-id="af9ea-105">當需要變更區域時，DVDPlay.exe 的應用程式也會啟動這個屬性頁面。</span><span class="sxs-lookup"><span data-stu-id="af9ea-105">This property page is also brought up by the DVDPlay.exe application when a region needs to be changed.</span></span> <span data-ttu-id="af9ea-106">這個屬性頁的 UI 與 DVDRgn.exe 的 UI 非常類似，而且地區設定之在作業系統中。</span><span class="sxs-lookup"><span data-stu-id="af9ea-106">The UI of this property page is very similar to that of DVDRgn.exe and it is regionalized in the operating system.</span></span>

<span data-ttu-id="af9ea-107">針對 RPC1 磁片磁碟機，Windows 作業系統元件會管理區域變更。</span><span class="sxs-lookup"><span data-stu-id="af9ea-107">For RPC1 drives, the Windows Operating System components manage region changes.</span></span> <span data-ttu-id="af9ea-108">RPC2 磁片磁碟機會在自己的硬體中維護區域設定。</span><span class="sxs-lookup"><span data-stu-id="af9ea-108">RPC2 drives maintain the region setting in their own hardware.</span></span> <span data-ttu-id="af9ea-109">在 RPC2 磁片磁碟機上耗盡允許的變更數目時，磁片磁碟機將無法執行變更區域的呼叫，而作業系統中的區域變更元件將會指出對使用者的變更。</span><span class="sxs-lookup"><span data-stu-id="af9ea-109">When the number of allowed changes are exhausted on a RPC2 drive, the drive will fail the call to change the region and the region-change component in the operating system will indicate that to the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af9ea-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="af9ea-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af9ea-111">Windows 中的 DVD 區域變更支援</span><span class="sxs-lookup"><span data-stu-id="af9ea-111">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



