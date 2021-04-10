---
title: IME 模式模型變更
description: 輸入法模式模型從每位使用者變更為每個執行緒
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781c322949f17d4d3313b6a9b7b5eff9b1e83b06
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316156"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a><span data-ttu-id="663a6-103">輸入法模式模型從每位使用者變更為每個執行緒</span><span class="sxs-lookup"><span data-stu-id="663a6-103">IME mode model changed from per-user to per-thread</span></span>

## <a name="platforms"></a><span data-ttu-id="663a6-104">平台</span><span class="sxs-lookup"><span data-stu-id="663a6-104">Platforms</span></span>

<dl> <span data-ttu-id="663a6-105">用戶端-Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="663a6-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="663a6-106">伺服器-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="663a6-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="663a6-107">Description</span><span class="sxs-lookup"><span data-stu-id="663a6-107">Description</span></span>

<span data-ttu-id="663a6-108">在 Windows 8 中，IME 轉換模式與輸入法（IME）模式是以使用者內容為基礎，而變更應用程式的模式會影響所有其他應用程式。</span><span class="sxs-lookup"><span data-stu-id="663a6-108">In Windows 8, the IME Conversion Mode and IME Sentence Mode were based on the User context, and changing the mode of an application affected all other applications.</span></span> <span data-ttu-id="663a6-109">您可以使用語言 [控制台] 的 [advanced settings] 區段中的 [讓我為每個應用程式視窗設定不同的輸入方法] 設定，來停用此行為。</span><span class="sxs-lookup"><span data-stu-id="663a6-109">This behavior could be disabled by using the "Let me set a different input method for each app window" setting in the advanced settings section of the language control panel.</span></span>

<span data-ttu-id="663a6-110">為了改善相容性，Windows 8.1 模式會儲存在輸入內容中，而不論「讓我為每個應用程式設定不同的輸入方法」控制項的設定為何。</span><span class="sxs-lookup"><span data-stu-id="663a6-110">In order to improve compatibility, in Windows 8.1 the modes are stored in an Input context regardless of how the "Let me set a different input method for each app window" control is set.</span></span> <span data-ttu-id="663a6-111">在 Windows 8.1 中，「讓我為每個應用程式視窗設定不同的輸入方法」設定只會影響輸入方法本身的選取專案。</span><span class="sxs-lookup"><span data-stu-id="663a6-111">In Windows 8.1, the "Let me set a different input method for each app window" setting affects only the selection of the input method itself.</span></span>

<span data-ttu-id="663a6-112">在應用程式啟動時，IME 模式會設定為下列預設值：</span><span class="sxs-lookup"><span data-stu-id="663a6-112">At application start up, the IME mode is set to the following defaults:</span></span>



|          | <span data-ttu-id="663a6-113">軟體輸入面板</span><span class="sxs-lookup"><span data-stu-id="663a6-113">Software input panel</span></span> | <span data-ttu-id="663a6-114">硬體鍵盤</span><span class="sxs-lookup"><span data-stu-id="663a6-114">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="663a6-115">KOR、JPN</span><span class="sxs-lookup"><span data-stu-id="663a6-115">KOR, JPN</span></span> | <span data-ttu-id="663a6-116">開啟</span><span class="sxs-lookup"><span data-stu-id="663a6-116">On</span></span>                   | <span data-ttu-id="663a6-117">關閉</span><span class="sxs-lookup"><span data-stu-id="663a6-117">Off</span></span>               |
| <span data-ttu-id="663a6-118">CHS、CHT</span><span class="sxs-lookup"><span data-stu-id="663a6-118">CHS,CHT</span></span>  | <span data-ttu-id="663a6-119">開啟</span><span class="sxs-lookup"><span data-stu-id="663a6-119">On</span></span>                   | <span data-ttu-id="663a6-120">開啟</span><span class="sxs-lookup"><span data-stu-id="663a6-120">On</span></span>                |



 

## <a name="manifestations"></a><span data-ttu-id="663a6-121">表現</span><span class="sxs-lookup"><span data-stu-id="663a6-121">Manifestations</span></span>

<span data-ttu-id="663a6-122">當使用者變更應用程式的 IME 模式時，變更不會影響其他應用程式。</span><span class="sxs-lookup"><span data-stu-id="663a6-122">When a user changes the IME mode on an application, the change doesn’t affect other applications.</span></span>

## <a name="resources"></a><span data-ttu-id="663a6-123">資源</span><span class="sxs-lookup"><span data-stu-id="663a6-123">Resources</span></span>

-   [<span data-ttu-id="663a6-124">IME 轉換模式值</span><span class="sxs-lookup"><span data-stu-id="663a6-124">IME Conversion Mode Values</span></span>](../intl/ime-conversion-mode-values.md)
-   [<span data-ttu-id="663a6-125">IME 句子模式值</span><span class="sxs-lookup"><span data-stu-id="663a6-125">IME Sentence Mode Values</span></span>](../intl/ime-sentence-mode-values.md)

 

 