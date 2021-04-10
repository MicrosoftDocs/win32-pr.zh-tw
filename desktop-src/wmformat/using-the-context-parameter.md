---
title: 使用內容參數
description: 使用內容參數
ms.assetid: 50e37c36-0ce1-4abd-bb25-f18bb164fdeb
keywords:
- Windows Media Format SDK，coNtext 參數
- Windows Media 格式 SDK，pvCoNtext 參數
- pvCoNtext 參數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084d7ac0f58d3f3e19ae6b1d6f990a1867988bcd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104092532"
---
# <a name="using-the-context-parameter"></a><span data-ttu-id="786d2-106">使用內容參數</span><span class="sxs-lookup"><span data-stu-id="786d2-106">Using the Context Parameter</span></span>

<span data-ttu-id="786d2-107">Windows Media 格式 SDK 使用的部分回呼會採用稱為 *pvCoNtext* 的參數。</span><span class="sxs-lookup"><span data-stu-id="786d2-107">Some of the callbacks used by the Windows Media Format SDK take a parameter called *pvContext*.</span></span> <span data-ttu-id="786d2-108">呼叫物件會沿著您在開始非同步動作的方法中指定的值傳遞。</span><span class="sxs-lookup"><span data-stu-id="786d2-108">The calling objects pass along the value you specify in the method that began the asynchronous action.</span></span> <span data-ttu-id="786d2-109">例如，當您呼叫 [**IWMReader：： Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)時，可以傳遞 *pvCoNtext* 的值。</span><span class="sxs-lookup"><span data-stu-id="786d2-109">For example, when you call [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), you can pass a value for *pvContext*.</span></span> <span data-ttu-id="786d2-110">當 reader 物件呼叫 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)方法來通知您的應用程式已開啟檔案時，它會傳遞您在呼叫中使用的任何值，以 **OnStatus** 的 *pvCoNtext* 參數 **開啟**。</span><span class="sxs-lookup"><span data-stu-id="786d2-110">When the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method is called by the reader object to notify your application that the file has been opened, it will pass whatever value you used in your call to **Open** as the *pvContext* parameter of **OnStatus**.</span></span> <span data-ttu-id="786d2-111">此內容參數可供您使用，且您可以用任何想要的方式來使用。</span><span class="sxs-lookup"><span data-stu-id="786d2-111">This context parameter is provided for your use and you can use it in any way you like.</span></span>

<span data-ttu-id="786d2-112">當多個物件需要共用相同的回呼時，最常使用 *pvCoNtext* 參數。</span><span class="sxs-lookup"><span data-stu-id="786d2-112">The *pvContext* parameter is most often used when multiple objects need to share the same callback.</span></span> <span data-ttu-id="786d2-113">例如，有數個物件使用 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 方法。</span><span class="sxs-lookup"><span data-stu-id="786d2-113">For example, several objects use the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method.</span></span> <span data-ttu-id="786d2-114">您可以使用 *pvCoNtext* ，藉由針對原始呼叫傳遞不同的 *pvCoNtext* 值，讓不同的物件共用一個 **OnStatus** 的執行。</span><span class="sxs-lookup"><span data-stu-id="786d2-114">You can use *pvContext* to enable the different objects to share one implementation of **OnStatus** by passing a different value for *pvContext* on your original call.</span></span> <span data-ttu-id="786d2-115">在 **OnStatus** 的執行中，您可以根據 *pvCoNtext* 的值來分支訊息處理邏輯。</span><span class="sxs-lookup"><span data-stu-id="786d2-115">In your implementation of **OnStatus**, you can branch the message handling logic based on the value of *pvContext*.</span></span>

## <a name="related-topics"></a><span data-ttu-id="786d2-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="786d2-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="786d2-117">**使用回呼方法**</span><span class="sxs-lookup"><span data-stu-id="786d2-117">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




