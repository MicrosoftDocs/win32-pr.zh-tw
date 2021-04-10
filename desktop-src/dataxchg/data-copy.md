---
title: 資料複製
description: 本節討論如何使用資料複製訊息，將資料從某個應用程式傳送到另一個應用程式。
ms.assetid: 10a50efe-f3d5-4c59-a084-69119ef86129
keywords:
- 資料複製，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f494e36387bbd25c2b8789b59fff3e3e687ea9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022078"
---
# <a name="data-copy"></a><span data-ttu-id="f036e-104">資料複製</span><span class="sxs-lookup"><span data-stu-id="f036e-104">Data Copy</span></span>

<span data-ttu-id="f036e-105">資料複製功能可讓您將資料從某個應用程式傳送到另一個應用程式。</span><span class="sxs-lookup"><span data-stu-id="f036e-105">The data copy feature enables you to send data from one application to another.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="f036e-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="f036e-106">In This Section</span></span>



| <span data-ttu-id="f036e-107">Name</span><span class="sxs-lookup"><span data-stu-id="f036e-107">Name</span></span>                                                      | <span data-ttu-id="f036e-108">描述</span><span class="sxs-lookup"><span data-stu-id="f036e-108">Description</span></span>                                                                                        |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f036e-109">使用資料複製</span><span class="sxs-lookup"><span data-stu-id="f036e-109">Using Data Copy</span></span>](using-data-copy.md)<br/>         | <span data-ttu-id="f036e-110">提供範例，示範如何在兩個應用程式之間傳送資訊。</span><span class="sxs-lookup"><span data-stu-id="f036e-110">Provides an example that demonstrates how to send information between two applications.</span></span><br/> |
| [<span data-ttu-id="f036e-111">資料複製參考</span><span class="sxs-lookup"><span data-stu-id="f036e-111">Data Copy Reference</span></span>](data-copy-reference.md)<br/> | <span data-ttu-id="f036e-112">包含 API 參考。</span><span class="sxs-lookup"><span data-stu-id="f036e-112">Contains the API reference.</span></span><br/>                                                             |



 

### <a name="data-copy-messages"></a><span data-ttu-id="f036e-113">資料複製訊息</span><span class="sxs-lookup"><span data-stu-id="f036e-113">Data Copy Messages</span></span>



| <span data-ttu-id="f036e-114">Name</span><span class="sxs-lookup"><span data-stu-id="f036e-114">Name</span></span>                                           | <span data-ttu-id="f036e-115">描述</span><span class="sxs-lookup"><span data-stu-id="f036e-115">Description</span></span>                                           |
|------------------------------------------------|-------------------------------------------------------|
| [<span data-ttu-id="f036e-116">**WM \_ COPYDATA**</span><span class="sxs-lookup"><span data-stu-id="f036e-116">**WM\_COPYDATA**</span></span>](wm-copydata.md)<br/> | <span data-ttu-id="f036e-117">傳送以將資料傳遞給另一個應用程式。</span><span class="sxs-lookup"><span data-stu-id="f036e-117">Sent to pass data to another application.</span></span> <br/> |



 

### <a name="data-copy-structures"></a><span data-ttu-id="f036e-118">資料複製結構</span><span class="sxs-lookup"><span data-stu-id="f036e-118">Data Copy Structures</span></span>



| <span data-ttu-id="f036e-119">Name</span><span class="sxs-lookup"><span data-stu-id="f036e-119">Name</span></span>                                                | <span data-ttu-id="f036e-120">描述</span><span class="sxs-lookup"><span data-stu-id="f036e-120">Description</span></span>                                                                                                       |
|-----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f036e-121">**COPYDATASTRUCT**</span><span class="sxs-lookup"><span data-stu-id="f036e-121">**COPYDATASTRUCT**</span></span>](/windows/win32/api/winuser/ns-winuser-copydatastruct)<br/> | <span data-ttu-id="f036e-122">包含由 [**WM \_ COPYDATA**](wm-copydata.md) 訊息傳遞給另一個應用程式的資料。</span><span class="sxs-lookup"><span data-stu-id="f036e-122">Contains data to be passed to another application by the [**WM\_COPYDATA**](wm-copydata.md) message.</span></span> <br/> |



 

 

 





