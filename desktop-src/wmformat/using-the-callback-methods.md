---
title: 使用回呼方法
description: 使用回呼方法
ms.assetid: 098cb90b-8c21-4692-a4f9-bacce042520a
keywords:
- Windows Media Format SDK，回呼方法
- Windows Media Format SDK，以非同步方式呼叫的方法
- 回呼方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d39201c101c9031a7157f79f6c12ec88f07decfc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681388"
---
# <a name="using-the-callback-methods"></a><span data-ttu-id="225be-106">使用回呼方法</span><span class="sxs-lookup"><span data-stu-id="225be-106">Using the Callback Methods</span></span>

<span data-ttu-id="225be-107">Windows Media 格式 SDK 中的數個介面包含以非同步方式呼叫的方法。</span><span class="sxs-lookup"><span data-stu-id="225be-107">Several interfaces in the Windows Media Format SDK contain methods that are called asynchronously.</span></span> <span data-ttu-id="225be-108">這些方法大多使用回呼函式，將資訊傳遞給控制應用程式。</span><span class="sxs-lookup"><span data-stu-id="225be-108">Most of these methods use callback functions to pass information to the controlling application.</span></span>

<span data-ttu-id="225be-109">下列各節說明有關使用回呼方法搭配 Windows Media Format SDK 的一些一般問題。</span><span class="sxs-lookup"><span data-stu-id="225be-109">The following sections describe some of the general issues regarding the use of callback methods with the Windows Media Format SDK.</span></span>



| <span data-ttu-id="225be-110">區段</span><span class="sxs-lookup"><span data-stu-id="225be-110">Section</span></span>                                                                          | <span data-ttu-id="225be-111">描述</span><span class="sxs-lookup"><span data-stu-id="225be-111">Description</span></span>                                                                                                                                                                                          |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="225be-112">使用 OnStatus 回呼</span><span class="sxs-lookup"><span data-stu-id="225be-112">Using the OnStatus Callback</span></span>](using-the-onstatus-callback.md)                   | <span data-ttu-id="225be-113">描述如何執行 [**IWMStatusCallback：： OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) 回呼方法，由數個物件用來通知應用程式的 SDK 作業進度。</span><span class="sxs-lookup"><span data-stu-id="225be-113">Describes how to implement the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method, which is used by several objects to advise applications of SDK operation progress.</span></span> |
| [<span data-ttu-id="225be-114">使用非同步呼叫的事件</span><span class="sxs-lookup"><span data-stu-id="225be-114">Using Events with Asynchronous Calls</span></span>](using-events-with-asynchronous-calls.md) | <span data-ttu-id="225be-115">描述在應用程式中處理非同步方法呼叫的常見技術。</span><span class="sxs-lookup"><span data-stu-id="225be-115">Describes a common technique to handle asynchronous method calls in an application.</span></span>                                                                                                                  |
| [<span data-ttu-id="225be-116">使用內容參數</span><span class="sxs-lookup"><span data-stu-id="225be-116">Using the Context Parameter</span></span>](using-the-context-parameter.md)                   | <span data-ttu-id="225be-117">介紹 *pvCoNtext* 參數，其由數個回呼及其呼叫方法所共用，並說明其使用方式。</span><span class="sxs-lookup"><span data-stu-id="225be-117">Introduces the *pvContext* parameter, shared by several callbacks and their calling methods, and explains how to use it.</span></span>                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="225be-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="225be-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="225be-119">**程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="225be-119">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




