---
title: 存根優化 ACF 屬性
description: 這些屬性可讓您將存根程式碼的大小和速度優化。
ms.assetid: 8c98b9ff-d91c-4a17-90c9-298f588e46c5
keywords:
- ACF MIDL、屬性、存根優化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209490d6064d134a51492afee39c501059879bab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839767"
---
# <a name="stub-optimization-acf-attributes"></a><span data-ttu-id="0a961-104">存根優化 ACF 屬性</span><span class="sxs-lookup"><span data-stu-id="0a961-104">Stub Optimization ACF Attributes</span></span>

<span data-ttu-id="0a961-105">這些屬性可讓您將存根程式碼的大小和速度優化。</span><span class="sxs-lookup"><span data-stu-id="0a961-105">These attributes enable you to optimize the size and speed of your stub code.</span></span>



| <span data-ttu-id="0a961-106">屬性</span><span class="sxs-lookup"><span data-stu-id="0a961-106">Attribute</span></span>                                    | <span data-ttu-id="0a961-107">使用方式</span><span class="sxs-lookup"><span data-stu-id="0a961-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a961-108">程式 [**代碼**](code.md)[**了 nocode**](nocode.md)</span><span class="sxs-lookup"><span data-stu-id="0a961-108">[**code**](code.md)[**nocode**](nocode.md)</span></span> | <span data-ttu-id="0a961-109">同時使用程式 [**代碼**](code.md) 和 [**了 nocode**](nocode.md) 屬性，以避免產生未使用函式的 stub 程式碼。</span><span class="sxs-lookup"><span data-stu-id="0a961-109">Use the [**code**](code.md) and [**nocode**](nocode.md) attributes together to avoid generating stub code for unused functions.</span></span> <span data-ttu-id="0a961-110">將 **了 nocode** 屬性套用至介面標頭，並將程式 **代碼** 屬性套用至用戶端應用程式將會執行的程式。</span><span class="sxs-lookup"><span data-stu-id="0a961-110">Apply the **nocode** attribute to the interface header, and apply the **code** attribute to those procedures that the client application will implement.</span></span> <span data-ttu-id="0a961-111">用戶端 stub 程式碼只會針對選取的程式產生。</span><span class="sxs-lookup"><span data-stu-id="0a961-111">Client stub code will be generated only for the selected procedures.</span></span>                                                                |
| [<span data-ttu-id="0a961-112">**優化**</span><span class="sxs-lookup"><span data-stu-id="0a961-112">**optimize**</span></span>](optimize.md)                 | <span data-ttu-id="0a961-113">藉由指定要使用混合模式或解讀方法封送處理的資料，可讓您微調 MIDL 編譯器在產生 stub 程式碼時所執行的優化層級。</span><span class="sxs-lookup"><span data-stu-id="0a961-113">Lets you fine-tune the level of optimization that the MIDL compiler performs when generating stub code, by specifying that data is to be marshaled by either the mixed-mode or interpreted method.</span></span> <span data-ttu-id="0a961-114">您可以將 [**optimize**](optimize.md) 屬性套用至介面或介面內選取的函式。</span><span class="sxs-lookup"><span data-stu-id="0a961-114">You can apply the [**optimize**](optimize.md) attribute to an interface or to selected functions within the interface.</span></span> <span data-ttu-id="0a961-115">在任一種情況下，其使用都會覆寫命令列優化以及任何預先存在的預設值。</span><span class="sxs-lookup"><span data-stu-id="0a961-115">In either case, its use will override the command-line optimizations and any pre-existing defaults.</span></span> |



 

 

 




