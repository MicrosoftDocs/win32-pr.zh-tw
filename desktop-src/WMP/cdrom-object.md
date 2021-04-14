---
title: Cdrom 物件
description: Cdrom 物件提供一種方式來存取磁片磁碟機中的 CD 或 DVD。
ms.assetid: 9045b130-3e08-4880-a4e7-79b704c4c1f9
keywords:
- Cdrom 物件 Windows Media Player
topic_type:
- apiref
api_name:
- Cdrom Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 17c2de88749b4dd4a0ab756b77866c16e8878486
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104311924"
---
# <a name="cdrom-object"></a><span data-ttu-id="0d435-104">Cdrom 物件</span><span class="sxs-lookup"><span data-stu-id="0d435-104">Cdrom Object</span></span>

<span data-ttu-id="0d435-105">**Cdrom** 物件提供一種方式來存取磁片磁碟機中的 CD 或 DVD。</span><span class="sxs-lookup"><span data-stu-id="0d435-105">The **Cdrom** object provides a way to access a CD or DVD in its drive.</span></span>

<span data-ttu-id="0d435-106">**Cdrom** 物件支援下列屬性。</span><span class="sxs-lookup"><span data-stu-id="0d435-106">The **Cdrom** object supports the following properties.</span></span>



| <span data-ttu-id="0d435-107">屬性</span><span class="sxs-lookup"><span data-stu-id="0d435-107">Property</span></span>                                   | <span data-ttu-id="0d435-108">描述</span><span class="sxs-lookup"><span data-stu-id="0d435-108">Description</span></span>                                                                                                                                             |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d435-109">driveSpecifier</span><span class="sxs-lookup"><span data-stu-id="0d435-109">driveSpecifier</span></span>](cdrom-drivespecifier.md) | <span data-ttu-id="0d435-110">抓取 CD 或 DVD 光碟機號。</span><span class="sxs-lookup"><span data-stu-id="0d435-110">Retrieves the CD or DVD drive letter.</span></span>                                                                                                                   |
| [<span data-ttu-id="0d435-111">播放清單</span><span class="sxs-lookup"><span data-stu-id="0d435-111">playlist</span></span>](cdrom-playlist.md)             | <span data-ttu-id="0d435-112">抓取 [播放清單](playlist-object.md) 物件，此物件代表 cd 上目前位於 cd 光碟機的曲目，或 DVD 的根層級標題專案。</span><span class="sxs-lookup"><span data-stu-id="0d435-112">Retrieves a [Playlist](playlist-object.md) object representing the tracks on the CD currently in the CD drive or the root-level title entries for DVD.</span></span> |



 

<span data-ttu-id="0d435-113">**Cdrom** 物件支援下列方法。</span><span class="sxs-lookup"><span data-stu-id="0d435-113">The **Cdrom** object supports the following method.</span></span>



| <span data-ttu-id="0d435-114">方法</span><span class="sxs-lookup"><span data-stu-id="0d435-114">Method</span></span>                   | <span data-ttu-id="0d435-115">描述</span><span class="sxs-lookup"><span data-stu-id="0d435-115">Description</span></span>                          |
|--------------------------|--------------------------------------|
| [<span data-ttu-id="0d435-116">彈出</span><span class="sxs-lookup"><span data-stu-id="0d435-116">eject</span></span>](cdrom-eject.md) | <span data-ttu-id="0d435-117">從磁片磁碟機中取出 CD 或 DVD。</span><span class="sxs-lookup"><span data-stu-id="0d435-117">Ejects the CD or DVD from the drive.</span></span> |



 

<span data-ttu-id="0d435-118">**Cdrom** 物件是透過下列方法來存取。</span><span class="sxs-lookup"><span data-stu-id="0d435-118">The **Cdrom** object is accessed through the following method.</span></span>



| <span data-ttu-id="0d435-119">Object</span><span class="sxs-lookup"><span data-stu-id="0d435-119">Object</span></span>                                        | <span data-ttu-id="0d435-120">方法</span><span class="sxs-lookup"><span data-stu-id="0d435-120">Method</span></span>                           |
|-----------------------------------------------|----------------------------------|
| [<span data-ttu-id="0d435-121">CdromCollection</span><span class="sxs-lookup"><span data-stu-id="0d435-121">CdromCollection</span></span>](cdromcollection-object.md) | [<span data-ttu-id="0d435-122">item</span><span class="sxs-lookup"><span data-stu-id="0d435-122">item</span></span>](cdromcollection-item.md) |



 

<span data-ttu-id="0d435-123">基於說明的目的，cdromCollection 會在參考語法區段中使用) 專案 (*索引* 。</span><span class="sxs-lookup"><span data-stu-id="0d435-123">For purposes of illustration, player.cdromCollection.item(*index*) is used in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d435-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d435-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d435-125">**腳本的物件模型參考**</span><span class="sxs-lookup"><span data-stu-id="0d435-125">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




