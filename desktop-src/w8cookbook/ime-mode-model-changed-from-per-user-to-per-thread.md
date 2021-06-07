---
title: IME 模式模型變更
description: 輸入法模式模型從每位使用者變更為每個執行緒
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30404b1a386c4346e7d8900481d8c5198972cdbe
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443244"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a><span data-ttu-id="e862a-103">輸入法模式模型從每位使用者變更為每個執行緒</span><span class="sxs-lookup"><span data-stu-id="e862a-103">IME mode model changed from per-user to per-thread</span></span>

## <a name="platforms"></a><span data-ttu-id="e862a-104">平台</span><span class="sxs-lookup"><span data-stu-id="e862a-104">Platforms</span></span>

<dl> <span data-ttu-id="e862a-105">用戶端-Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="e862a-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="e862a-106">伺服器-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e862a-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="e862a-107">描述</span><span class="sxs-lookup"><span data-stu-id="e862a-107">Description</span></span>

<span data-ttu-id="e862a-108">在 Windows 8 中，IME 轉換模式與輸入法（IME）模式是以使用者內容為基礎，而變更應用程式的模式會影響所有其他應用程式。</span><span class="sxs-lookup"><span data-stu-id="e862a-108">In Windows 8, the IME Conversion Mode and IME Sentence Mode were based on the User context, and changing the mode of an application affected all other applications.</span></span> <span data-ttu-id="e862a-109">您可以使用語言 [控制台] 的 [advanced settings] 區段中的 [讓我為每個應用程式視窗設定不同的輸入方法] 設定，來停用此行為。</span><span class="sxs-lookup"><span data-stu-id="e862a-109">This behavior could be disabled by using the "Let me set a different input method for each app window" setting in the advanced settings section of the language control panel.</span></span>

<span data-ttu-id="e862a-110">為了改善相容性，Windows 8.1 模式會儲存在輸入內容中，而不論「讓我為每個應用程式設定不同的輸入方法」控制項的設定為何。</span><span class="sxs-lookup"><span data-stu-id="e862a-110">In order to improve compatibility, in Windows 8.1 the modes are stored in an Input context regardless of how the "Let me set a different input method for each app window" control is set.</span></span> <span data-ttu-id="e862a-111">在 Windows 8.1 中，「讓我為每個應用程式視窗設定不同的輸入方法」設定只會影響輸入方法本身的選取專案。</span><span class="sxs-lookup"><span data-stu-id="e862a-111">In Windows 8.1, the "Let me set a different input method for each app window" setting affects only the selection of the input method itself.</span></span>

<span data-ttu-id="e862a-112">在應用程式啟動時，IME 模式會設定為下列預設值：</span><span class="sxs-lookup"><span data-stu-id="e862a-112">At application start up, the IME mode is set to the following defaults:</span></span>



| &nbsp;   | <span data-ttu-id="e862a-113">軟體輸入面板</span><span class="sxs-lookup"><span data-stu-id="e862a-113">Software input panel</span></span> | <span data-ttu-id="e862a-114">硬體鍵盤</span><span class="sxs-lookup"><span data-stu-id="e862a-114">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="e862a-115">KOR、JPN</span><span class="sxs-lookup"><span data-stu-id="e862a-115">KOR, JPN</span></span> | <span data-ttu-id="e862a-116">開啟</span><span class="sxs-lookup"><span data-stu-id="e862a-116">On</span></span>                   | <span data-ttu-id="e862a-117">關閉</span><span class="sxs-lookup"><span data-stu-id="e862a-117">Off</span></span>               |
| <span data-ttu-id="e862a-118">CHS、CHT</span><span class="sxs-lookup"><span data-stu-id="e862a-118">CHS,CHT</span></span>  | <span data-ttu-id="e862a-119">開啟</span><span class="sxs-lookup"><span data-stu-id="e862a-119">On</span></span>                   | <span data-ttu-id="e862a-120">開啟</span><span class="sxs-lookup"><span data-stu-id="e862a-120">On</span></span>                |



 

## <a name="manifestations"></a><span data-ttu-id="e862a-121">表現</span><span class="sxs-lookup"><span data-stu-id="e862a-121">Manifestations</span></span>

<span data-ttu-id="e862a-122">當使用者變更應用程式的 IME 模式時，變更不會影響其他應用程式。</span><span class="sxs-lookup"><span data-stu-id="e862a-122">When a user changes the IME mode on an application, the change doesn’t affect other applications.</span></span>

## <a name="resources"></a><span data-ttu-id="e862a-123">資源</span><span class="sxs-lookup"><span data-stu-id="e862a-123">Resources</span></span>

-   [<span data-ttu-id="e862a-124">IME 轉換模式值</span><span class="sxs-lookup"><span data-stu-id="e862a-124">IME Conversion Mode Values</span></span>](../intl/ime-conversion-mode-values.md)
-   [<span data-ttu-id="e862a-125">IME 句子模式值</span><span class="sxs-lookup"><span data-stu-id="e862a-125">IME Sentence Mode Values</span></span>](../intl/ime-sentence-mode-values.md)

 

 