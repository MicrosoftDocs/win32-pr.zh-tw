---
title: 移植鳶尾花 GL Get 函數
description: 鳶尾花 GL \ 0034; get \ 0034;函數採用下列形式
ms.assetid: 5bd6aa13-b41d-4f89-91dc-cc47481ac7b7
keywords:
- 鳶尾花 GL 移植，取得函式
- 從鳶尾花 GL 進行移植，取得函數
- 從鳶尾花 GL 移植至 OpenGL，取得函數
- 從鳶尾花 GL 進行 OpenGL 移植，取得函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594b12bb1738846b98d33137dd8b623f0405ec40
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965597"
---
# <a name="porting-iris-gl-get-functions"></a><span data-ttu-id="ca83a-107">移植鳶尾花 GL Get 函數</span><span class="sxs-lookup"><span data-stu-id="ca83a-107">Porting IRIS GL Get Functions</span></span>

<span data-ttu-id="ca83a-108">鳶尾花 GL "get" 函式採用下列格式：</span><span class="sxs-lookup"><span data-stu-id="ca83a-108">IRIS GL "get" functions take the following form:</span></span>

``` syntax
int getthing();
```

<span data-ttu-id="ca83a-109">及</span><span class="sxs-lookup"><span data-stu-id="ca83a-109">and</span></span>

``` syntax
int getthings( int *a, int *b);
```

<span data-ttu-id="ca83a-110">您的鳶尾花 GL 程式碼可能包含如下所示的 get 函式呼叫：</span><span class="sxs-lookup"><span data-stu-id="ca83a-110">Your IRIS GL code probably includes get function calls that look something like:</span></span>

``` syntax
thing = getthing(); 
if (getthing() == THING) { /* some stuff here */ } 
getthings (&a, &b);
```

<span data-ttu-id="ca83a-111">在 OpenGL 中，您可以使用下列四種類型的 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) 函式之一來取代相等的鳶尾花 GL get 函式：</span><span class="sxs-lookup"><span data-stu-id="ca83a-111">In OpenGL you use one of the following four types of [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) functions in place of equivalent IRIS GL get functions:</span></span>

-   <span data-ttu-id="ca83a-112">**glGetBooleanv**</span><span class="sxs-lookup"><span data-stu-id="ca83a-112">**glGetBooleanv**</span></span>
-   <span data-ttu-id="ca83a-113">**glGetIntegerv**</span><span class="sxs-lookup"><span data-stu-id="ca83a-113">**glGetIntegerv**</span></span>
-   <span data-ttu-id="ca83a-114">**glGetFloatv**</span><span class="sxs-lookup"><span data-stu-id="ca83a-114">**glGetFloatv**</span></span>
-   <span data-ttu-id="ca83a-115">**glGetDoublev**</span><span class="sxs-lookup"><span data-stu-id="ca83a-115">**glGetDoublev**</span></span>

<span data-ttu-id="ca83a-116">這些函數具有下列語法：</span><span class="sxs-lookup"><span data-stu-id="ca83a-116">The functions have the following syntax:</span></span>

``` syntax
glGet<Datatype>v( value, *data );
```

<span data-ttu-id="ca83a-117">其中 *值* 的型別為 **GLenum** ，而資料的型別為 **GLdatatype**。</span><span class="sxs-lookup"><span data-stu-id="ca83a-117">where *value* is of type **GLenum** and data is of type **GLdatatype**.</span></span> <span data-ttu-id="ca83a-118">當您呼叫 **glGet** 時，它會傳回與預期型別不同的類型，類型會適當地進行轉換。</span><span class="sxs-lookup"><span data-stu-id="ca83a-118">When you call **glGet** and it returns a type different from the type expected, the type is converted appropriately.</span></span> <span data-ttu-id="ca83a-119">如需 **glGet** 參數的完整清單，請參閱 [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)。</span><span class="sxs-lookup"><span data-stu-id="ca83a-119">For a complete list of **glGet** parameters, see [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md).</span></span>

 

 




