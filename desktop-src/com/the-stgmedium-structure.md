---
title: STGMEDIUM 結構
description: STGMEDIUM 結構
ms.assetid: ff1e1128-d228-45a6-a19d-2875b6c4e003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86faf52ab93bab39b8413ea2eb6381da24b643b5
ms.sourcegitcommit: 89f99926f946dc6c5ea600fb7c41f6b19ceac516
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2020
ms.locfileid: "104024310"
---
# <a name="the-stgmedium-structure"></a><span data-ttu-id="0ed25-103">STGMEDIUM 結構</span><span class="sxs-lookup"><span data-stu-id="0ed25-103">The STGMEDIUM Structure</span></span>

<span data-ttu-id="0ed25-104">如同 [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) 結構是 Windows 剪貼簿格式識別碼的增強功能，因此 [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) 結構是用來傳輸資料的全域記憶體控制碼的改進。</span><span class="sxs-lookup"><span data-stu-id="0ed25-104">Just as the [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) structure is an enhancement of the Windows clipboard format identifier, so the [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) structure is an improvement of the global memory handle used to transfer the data.</span></span> <span data-ttu-id="0ed25-105">**STGMEDIUM** 結構包括成員 **tymed**，這表示要使用的媒體，以及組成指標的等位，以及取得 **tymed** 中指定之媒體的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0ed25-105">The **STGMEDIUM** structure includes a member, **tymed**, which indicates the medium to be used, and a union comprising pointers and a handle for getting whichever medium is specified in **tymed**.</span></span>

<span data-ttu-id="0ed25-106">[**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)結構可讓資料來源和取用者以每個轉譯為基礎，選擇最有效率的 exchange 媒體。</span><span class="sxs-lookup"><span data-stu-id="0ed25-106">The [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) structure enables both data sources and consumers to choose the most efficient exchange medium on a per-rendering basis.</span></span> <span data-ttu-id="0ed25-107">如果資料很大，而應該保留在磁片上，則資料來源可以用慣用的格式指出磁片型媒體，而只有在這是取用者瞭解的唯一媒介時，才使用全域記憶體作為備份。</span><span class="sxs-lookup"><span data-stu-id="0ed25-107">If the data is so large that it should be kept on disk, the data source can indicate a disk-based medium in its preferred format, only using global memory as a backup if that's the only medium the consumer understands.</span></span> <span data-ttu-id="0ed25-108">能夠使用最適合交換的媒體作為預設值，可改善應用程式之間資料交換的整體效能。</span><span class="sxs-lookup"><span data-stu-id="0ed25-108">Being able to use the best medium for exchanges as the default improves overall performance of data exchange between applications.</span></span> <span data-ttu-id="0ed25-109">例如，如果要傳送的部分資料已在磁片上，則來源應用程式可以在相同的應用程式中移動或複製到新的目的地，而不需要先將資料載入至全域記憶體。</span><span class="sxs-lookup"><span data-stu-id="0ed25-109">For example, if some of the data to be transferred is already on disk, the source application can move or copy it to a new destination, either in the same application or in some other, without having first to load the data into global memory.</span></span> <span data-ttu-id="0ed25-110">在接收端，資料的取用者不需要將它寫回磁片。</span><span class="sxs-lookup"><span data-stu-id="0ed25-110">At the receiving end, the consumer of the data does not have to write it back to disk.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ed25-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ed25-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ed25-112">資料格式和傳輸媒體</span><span class="sxs-lookup"><span data-stu-id="0ed25-112">Data Formats and Transfer Media</span></span>](data-formats-and-transfer-media.md)
</dt> </dl>

 

 




