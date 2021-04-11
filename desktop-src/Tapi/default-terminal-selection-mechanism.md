---
description: Multitrack 終端機的概念讓 TAPI 更適合用來提供簡化的方法，讓您選取串流或串流上的終端機。 預設終端機選取機制的設計目的是要解決此情況。
ms.assetid: fbdc7359-b44e-4605-baea-eef5155340c7
title: 預設終端機選取機制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5512797434fac028e91bf64a88bb9a22b8968c87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847859"
---
# <a name="default-terminal-selection-mechanism"></a><span data-ttu-id="0476e-104">預設終端機選取機制</span><span class="sxs-lookup"><span data-stu-id="0476e-104">Default Terminal Selection Mechanism</span></span>

<span data-ttu-id="0476e-105">[Multitrack 終端](multitrack-terminals.md)機的概念讓 TAPI 更適合用來提供簡化的方法，讓您選取串流或串流上的終端機。</span><span class="sxs-lookup"><span data-stu-id="0476e-105">The concept of [multitrack terminal](multitrack-terminals.md) makes it even more desirable for TAPI to provide a simplified method of selecting a terminal on a stream or streams.</span></span> <span data-ttu-id="0476e-106">預設終端機選取機制的設計目的是要解決此情況。</span><span class="sxs-lookup"><span data-stu-id="0476e-106">The Default Terminal Selection mechanism is designed to address this.</span></span>

## <a name="selecting-a-terminal-on-a-call"></a><span data-ttu-id="0476e-107">選取來電上的終端機</span><span class="sxs-lookup"><span data-stu-id="0476e-107">Selecting a Terminal on a Call</span></span>

<span data-ttu-id="0476e-108">預設的終端機選取功能是透過在通話時選取終端機的功能所提供。</span><span class="sxs-lookup"><span data-stu-id="0476e-108">The Default Terminal Selection feature is provided via the ability to select a terminal on a call.</span></span>

<span data-ttu-id="0476e-109">[呼叫物件](call-object.md)會公開新的介面 [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2)。</span><span class="sxs-lookup"><span data-stu-id="0476e-109">The [call object](call-object.md) exposes a new interface, [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2).</span></span> <span data-ttu-id="0476e-110">介面會公開與 [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol)相同的方法，加上三個新的方法： [**RequestTerminal**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-requestterminal)、 [**SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall)和 [**UnselectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall)。</span><span class="sxs-lookup"><span data-stu-id="0476e-110">The interface exposes the same methods as [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol), plus three new methods: [**RequestTerminal**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-requestterminal), [**SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall), and [**UnselectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall).</span></span>

<span data-ttu-id="0476e-111">**ITBasicCallControl2：： RequestTerminal** 會建立終端機，並提供終端機類別、方向和媒體類型。</span><span class="sxs-lookup"><span data-stu-id="0476e-111">**ITBasicCallControl2::RequestTerminal** creates a terminal, given the terminal class, direction, and media type.</span></span> <span data-ttu-id="0476e-112">它會查看支援的靜態和動態終端機清單，以尋找並建立要求的終端機。</span><span class="sxs-lookup"><span data-stu-id="0476e-112">It looks through the lists of supported static and dynamic terminals to find and create the requested terminal.</span></span>

<span data-ttu-id="0476e-113">[**ITBasicCallControl2：： SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) 會選取終端 (或者在 multitrack 終端機、列舉、視需要建立，然後選取資料流程 (的追蹤終端機) ，或可在呼叫上取得的資料流程) 。</span><span class="sxs-lookup"><span data-stu-id="0476e-113">[**ITBasicCallControl2::SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) selects the terminal (or, in the case of a multitrack terminal, enumerates, creates if needed, and selects the track terminals) on the stream (or streams) available on the call.</span></span>

<span data-ttu-id="0476e-114">[**ITBasicCallControl2：： SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall)的檔將說明將呼叫串流用於比對終端機 (或追蹤可在終端機) 上使用的演算法。</span><span class="sxs-lookup"><span data-stu-id="0476e-114">The algorithm for matching call streams to the terminal (or tracks available on the terminal) is described in the documentation for [**ITBasicCallControl2::SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall).</span></span>

<span data-ttu-id="0476e-115">呼叫 [**ITBasicCallControl2：： UnselectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall) 會導致終端機 (單一追蹤或 multitrack) 從呼叫中取消選取。</span><span class="sxs-lookup"><span data-stu-id="0476e-115">Calling [**ITBasicCallControl2::UnselectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-unselectterminaloncall) causes the terminal (single-track or multitrack) to be unselected from the call.</span></span> <span data-ttu-id="0476e-116">如需詳細資訊，請參閱方法的檔。</span><span class="sxs-lookup"><span data-stu-id="0476e-116">See the method's documentation for more details.</span></span>

## <a name="selecting-a-terminal-on-itstream"></a><span data-ttu-id="0476e-117">選取 ITStream 上的終端機</span><span class="sxs-lookup"><span data-stu-id="0476e-117">Selecting a Terminal on ITStream</span></span>

<span data-ttu-id="0476e-118">藉由呼叫 [**ITStream：：) SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal)選取 [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) (上的單一追蹤終端機，會選取資料流程上的終端機。</span><span class="sxs-lookup"><span data-stu-id="0476e-118">Selecting a single-track terminal on [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) (by calling [**ITStream::SelectTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itstream-selectterminal)) selects the terminal on the stream.</span></span> <span data-ttu-id="0476e-119">這是一般的 TAPI 3 終端機選擇程式。</span><span class="sxs-lookup"><span data-stu-id="0476e-119">This is the usual TAPI 3 terminal selection procedure.</span></span>

<span data-ttu-id="0476e-120">只可在資料流程上選取單一追蹤終端機。</span><span class="sxs-lookup"><span data-stu-id="0476e-120">Only single-tracks terminals can be selected on a stream.</span></span> <span data-ttu-id="0476e-121">選取串流上的 multitrack 終端機將會失敗，因為資料流程將無法辨識媒體類型和方向。</span><span class="sxs-lookup"><span data-stu-id="0476e-121">Selecting a multitrack terminal on a stream will fail, because the stream will not recognize the media type and direction.</span></span>

 

 
