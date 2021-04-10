---
title: 建立具有多個會話的光碟
description: IMAPI.EXE 能夠建立多會話資料光碟。 建立多會話光碟時，有幾個需要注意的事項。
ms.assetid: 02405a32-53d5-4618-bfa0-c9a9f5e3c51b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc41dba861ce29bd3d3e25e33ba0ba5ab5bf38a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183345"
---
# <a name="creating-discs-with-multiple-sessions"></a><span data-ttu-id="44f60-104">建立具有多個會話的光碟</span><span class="sxs-lookup"><span data-stu-id="44f60-104">Creating Discs with Multiple Sessions</span></span>

<span data-ttu-id="44f60-105">IMAPI.EXE 能夠建立多會話資料光碟。</span><span class="sxs-lookup"><span data-stu-id="44f60-105">IMAPI is capable of creating multi-session data discs.</span></span> <span data-ttu-id="44f60-106">建立多會話光碟時，有幾個需要注意的事項。</span><span class="sxs-lookup"><span data-stu-id="44f60-106">There are a few considerations to be aware of when creating a multi-session disc.</span></span>

<span data-ttu-id="44f60-107">[**IDiscMaster：： SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder)方法會判斷在設定時是否有使用中磁片磁碟機的 imapi.exe 多會話光碟。</span><span class="sxs-lookup"><span data-stu-id="44f60-107">The [**IDiscMaster::SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder) method determines whether there is an IMAPI multi-session disc in the active drive upon setting.</span></span> <span data-ttu-id="44f60-108">如果是，IMAPI.EXE 會自動進入多會話模式。</span><span class="sxs-lookup"><span data-stu-id="44f60-108">If so, IMAPI goes into multi-session mode automatically.</span></span> <span data-ttu-id="44f60-109">在建立多會話模式後使用 [**ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) 會導致 imapi.exe 回到單一會話模式。</span><span class="sxs-lookup"><span data-stu-id="44f60-109">Using [**ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) after multi-session mode has been established causes IMAPI to return to single-session mode.</span></span> <span data-ttu-id="44f60-110">這表示 [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) 燒錄需要空白光碟。</span><span class="sxs-lookup"><span data-stu-id="44f60-110">This means that a blank disc is required for a [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) burn.</span></span> <span data-ttu-id="44f60-111">如果光碟處於多重會話模式，則相同的光碟必須在使用中的錄製器中，否則將會傳回 IMAPI.EXE \_ E \_ WRONGDISC 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="44f60-111">If the disc is in multi-session mode, the same disc must be in the active recorder or an error code of IMAPI\_E\_WRONGDISC will be returned.</span></span>

<span data-ttu-id="44f60-112">在 Joliet 格式中選取錄製器，會讓 IMAPI.EXE 從目前安裝的光碟讀取資訊。如果光碟是另一個會話具有空間的先前 IMAPI.EXE Joliet 光碟，IMAPI.EXE 會自動將自己設定為多會話模式。</span><span class="sxs-lookup"><span data-stu-id="44f60-112">Selecting a recorder while in Joliet format causes IMAPI to read information from the currently installed disc. If the disc is a previous IMAPI Joliet disc that has space for another session, IMAPI automatically sets itself to multi-session mode.</span></span> <span data-ttu-id="44f60-113">呼叫 [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc)時，此光碟必須存在於使用中的錄製器中。</span><span class="sxs-lookup"><span data-stu-id="44f60-113">This disc must be present in the active recorder when calling [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc).</span></span>

<span data-ttu-id="44f60-114">關閉光碟上的第一個會話需要 21 MB。</span><span class="sxs-lookup"><span data-stu-id="44f60-114">Closing the first session on a disc requires 21 MB.</span></span> <span data-ttu-id="44f60-115">每個額外的會話都需要 11 MB 來關閉。</span><span class="sxs-lookup"><span data-stu-id="44f60-115">Each additional session requires 11 MB to close.</span></span>

 

 




