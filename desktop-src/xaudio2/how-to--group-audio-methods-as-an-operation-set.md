---
description: 本主題將說明如何將 XAudio2 方法群組在一起，讓它們可以同時生效。
ms.assetid: 1b50acc5-a6b2-e010-9e7e-0080a5ee4a58
title: 使用方法：將音訊方法群組為操作集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5146c650ae6f89331c40f3e0db896f49484a6f0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850368"
---
# <a name="how-to-group-audio-methods-as-an-operation-set"></a><span data-ttu-id="2d706-103">使用方法：將音訊方法群組為操作集</span><span class="sxs-lookup"><span data-stu-id="2d706-103">How to: Group Audio Methods as an Operation Set</span></span>

<span data-ttu-id="2d706-104">本主題將說明如何將 XAudio2 方法群組在一起，讓它們可以同時生效。</span><span class="sxs-lookup"><span data-stu-id="2d706-104">This topic shows you how you can group together XAudio2 methods so they take effect at the same time.</span></span>

## <a name="to-group-audio-methods-as-an-operation-set"></a><span data-ttu-id="2d706-105">將音訊方法分組為操作集</span><span class="sxs-lookup"><span data-stu-id="2d706-105">To group audio methods as an operation set</span></span>

1.  <span data-ttu-id="2d706-106">宣告全域操作集計數器。</span><span class="sxs-lookup"><span data-stu-id="2d706-106">Declare a global operation set counter.</span></span>

    <span data-ttu-id="2d706-107">[Operation set](operation-sets.md)計數器可確保每個操作集都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="2d706-107">The [operation set](operation-sets.md) counter ensures that each operation set is unique.</span></span>

    ```
    UINT32 OperationSetCounter = 0;
    ```

    

2.  <span data-ttu-id="2d706-108">遞增全域計數器。</span><span class="sxs-lookup"><span data-stu-id="2d706-108">Increment the global counter.</span></span>

    <span data-ttu-id="2d706-109">每次提交新的作業 [集](operation-sets.md)時，全域計數器應該會遞增，以確保每個集合都是唯一的。</span><span class="sxs-lookup"><span data-stu-id="2d706-109">Each time you submit a new [operation set](operation-sets.md), the global counter should increment to ensure each set is unique.</span></span>

    ```
    UINT32 OperationID = UINT32(InterlockedIncrement(LPLONG(&OperationSetCounter)));
    ```

    

3.  <span data-ttu-id="2d706-110">藉由設定其作業 [集](operation-sets.md) 參數，將方法呼叫分組。</span><span class="sxs-lookup"><span data-stu-id="2d706-110">Group the method calls by setting their [operation set](operation-sets.md) parameters.</span></span>

4.  <span data-ttu-id="2d706-111">將 [operation set](operation-sets.md) 參數設定為 global 計數器的目前值。</span><span class="sxs-lookup"><span data-stu-id="2d706-111">Set the [operation set](operation-sets.md) parameters to the current value of the global counter.</span></span>

    <span data-ttu-id="2d706-112">在此情況下， [**IXAudio2SourceVoice：： Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) 的四個呼叫會分組為一個作業 [集](operation-sets.md)。</span><span class="sxs-lookup"><span data-stu-id="2d706-112">In this case, four calls to [**IXAudio2SourceVoice::Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) are grouped as one [operation set](operation-sets.md).</span></span> <span data-ttu-id="2d706-113">將通話分組會導致所有四個音效都在相同的時間內啟動。</span><span class="sxs-lookup"><span data-stu-id="2d706-113">Grouping the calls causes all four of the sounds to start at exactly the same time.</span></span>

    ```
    hr = pSFXSourceVoice1->Start( 0, OperationID );
    hr = pSFXSourceVoice2->Start( 0, OperationID );
    hr = pSFXSourceVoice3->Start( 0, OperationID );
    hr = pSFXSourceVoice4->Start( 0, OperationID );
    ```

    

5.  <span data-ttu-id="2d706-114">開始 [操作集](operation-sets.md)。</span><span class="sxs-lookup"><span data-stu-id="2d706-114">Start the [operation set](operation-sets.md).</span></span>

    <span data-ttu-id="2d706-115">當您呼叫集合中的所有方法之後，請呼叫 [**IXAudio2：： CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) ，並以全域計數器的目前值來啟動 set。</span><span class="sxs-lookup"><span data-stu-id="2d706-115">After you call all the methods in the set, start the set by calling [**IXAudio2::CommitChanges**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-commitchanges) with the current value of the global counter.</span></span>

    ```
    pXAudio2->CommitChanges(OperationID);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="2d706-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="2d706-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d706-117">操作集</span><span class="sxs-lookup"><span data-stu-id="2d706-117">Operation Sets</span></span>](operation-sets.md)
</dt> <dt>

[<span data-ttu-id="2d706-118">XAudio2 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="2d706-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="2d706-119">XAudio2 操作集</span><span class="sxs-lookup"><span data-stu-id="2d706-119">XAudio2 Operation Sets</span></span>](xaudio2-operation-sets.md)
</dt> </dl>

 

 
