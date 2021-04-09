---
title: 隨選安裝的 Windows 元件
description: 隨選安裝的 Windows 元件
ms.assetid: 14865DD7-167C-462C-B85A-BD07C929D7B8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d2c3c3fee1cd12d7b12900e41dc006badcf53f
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104024224"
---
# <a name="windows-components-installed-on-demand"></a><span data-ttu-id="1afdc-103">隨選安裝的 Windows 元件</span><span class="sxs-lookup"><span data-stu-id="1afdc-103">Windows components installed on demand</span></span>

## <a name="platform"></a><span data-ttu-id="1afdc-104">平台</span><span class="sxs-lookup"><span data-stu-id="1afdc-104">Platform</span></span>

<span data-ttu-id="1afdc-105">**用戶端-** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1afdc-105">**Clients -** Windows 8.1</span></span>  







## <a name="description"></a><span data-ttu-id="1afdc-106">Description</span><span class="sxs-lookup"><span data-stu-id="1afdc-106">Description</span></span>

<span data-ttu-id="1afdc-107">Windows 8.1： DirectPlay 和 NTVDM 將依需求安裝兩個 Windows 元件。</span><span class="sxs-lookup"><span data-stu-id="1afdc-107">Two Windows components will be installed on demand in Windows 8.1: DirectPlay and NTVDM.</span></span> <span data-ttu-id="1afdc-108">這些元件會列在 [舊版元件] 節點下的 [選用元件] 中。</span><span class="sxs-lookup"><span data-stu-id="1afdc-108">These components are listed within Optional Components under the “Legacy Components” node.</span></span> <span data-ttu-id="1afdc-109">這些元件會在本機安裝為作業系統的一部分，並壓縮為選用元件。</span><span class="sxs-lookup"><span data-stu-id="1afdc-109">These components are installed locally as part of the operating system, and compressed as optional components.</span></span> <span data-ttu-id="1afdc-110">當應用程式參考或呼叫其中一個元件時 (通常是在第一次啟動應用程式) 時自動觸發安裝。</span><span class="sxs-lookup"><span data-stu-id="1afdc-110">When an app references or calls one of these components (usually at first launch of the app), installation is triggered automatically.</span></span> <span data-ttu-id="1afdc-111">使用者將會收到安裝元件的通知，且必須確認動作才能繼續。</span><span class="sxs-lookup"><span data-stu-id="1afdc-111">Users will be notified that the component will be installed, and they must confirm the action in order to proceed.</span></span> <span data-ttu-id="1afdc-112">如果使用者不是系統管理員，則需要提高許可權才能順利完成。</span><span class="sxs-lookup"><span data-stu-id="1afdc-112">Elevation is required for this to succeed if the user is not an administrator.</span></span> <span data-ttu-id="1afdc-113">初始安裝之後，使用者不需要執行任何其他動作，也可以再次使用該元件。</span><span class="sxs-lookup"><span data-stu-id="1afdc-113">After the initial installation, the user does not need to perform any other actions to use the component again.</span></span>

## <a name="manifestation"></a><span data-ttu-id="1afdc-114">表現</span><span class="sxs-lookup"><span data-stu-id="1afdc-114">Manifestation</span></span>

<span data-ttu-id="1afdc-115">當應用程式在第一次啟動) 時，于選用元件中參考或呼叫舊版元件 (時，應用程式將會暫停，並會開啟 [視需要提供功能] 對話方塊，要求使用者安裝元件的許可權。</span><span class="sxs-lookup"><span data-stu-id="1afdc-115">When an app references or calls a legacy component in optional components (at first launch), the app will be suspended and the Feature on Demand dialog will open, requesting user permission to install the component.</span></span> <span data-ttu-id="1afdc-116">如果使用者按一下 [確定]，他們也可能會看到提高許可權提示，其中必須輸入其認證。</span><span class="sxs-lookup"><span data-stu-id="1afdc-116">If users click OK, they may also see an elevation prompt where they must enter their credentials.</span></span> <span data-ttu-id="1afdc-117">然後會安裝元件，然後應用程式會繼續執行。</span><span class="sxs-lookup"><span data-stu-id="1afdc-117">The component will then be installed and the app will resume.</span></span>

## <a name="mitigation"></a><span data-ttu-id="1afdc-118">降低</span><span class="sxs-lookup"><span data-stu-id="1afdc-118">Mitigation</span></span>

<span data-ttu-id="1afdc-119">若要讓功能隨選 UI 開啟，您可以使用 DISM 或選擇性元件 UI 來預先安裝 DirectPlay 和 NTVDM。</span><span class="sxs-lookup"><span data-stu-id="1afdc-119">To keep the Features on Demand UI from opening, you can pre-install DirectPlay and NTVDM using DISM or the Optional Components UI.</span></span>

## <a name="solution"></a><span data-ttu-id="1afdc-120">解決方法</span><span class="sxs-lookup"><span data-stu-id="1afdc-120">Solution</span></span>

<span data-ttu-id="1afdc-121">強烈建議您避免在未來的應用程式版本中，參考或呼叫已列為 Windows 舊版選用元件的元件。</span><span class="sxs-lookup"><span data-stu-id="1afdc-121">You are strongly encouraged to avoid referencing or calling components that have been listed as Legacy Optional Components in Windows in future versions of your app.</span></span> <span data-ttu-id="1afdc-122">舊版的選擇性元件只會包含較舊且較少使用的元件，而這些元件可能會造成使用者的效能和安全性問題。</span><span class="sxs-lookup"><span data-stu-id="1afdc-122">Legacy Optional Components will only include older, lesser-used components that could potentially cause performance and security issues for users.</span></span>

## <a name="tests"></a><span data-ttu-id="1afdc-123">測試</span><span class="sxs-lookup"><span data-stu-id="1afdc-123">Tests</span></span>

<span data-ttu-id="1afdc-124">不需要額外的測試住宿來提供相容性。</span><span class="sxs-lookup"><span data-stu-id="1afdc-124">No additional test accommodations are necessary for compatibility.</span></span> <span data-ttu-id="1afdc-125">請務必注意，當呼叫或參考選擇性元件時，此對話方塊會出現，而且此安裝需要提高許可權。</span><span class="sxs-lookup"><span data-stu-id="1afdc-125">It is important to be aware that this dialog will appear when the optional component is called or referenced, and this installation requires elevation.</span></span>

 

 




