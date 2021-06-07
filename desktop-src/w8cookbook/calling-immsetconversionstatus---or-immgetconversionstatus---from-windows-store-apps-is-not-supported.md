---
title: '不支援從 Windows Store 應用程式呼叫 ImmSetConversionStatus () 或 ImmGetConversionStatus () '
description: '不支援從 Windows Store 應用程式呼叫 ImmSetConversionStatus () 或 ImmGetConversionStatus () '
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8ca572b1ea88ca988ecba66231a87cb6ae6db2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443142"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a><span data-ttu-id="c37f3-103">不支援從 Windows Store 應用程式呼叫 ImmSetConversionStatus () 或 ImmGetConversionStatus () </span><span class="sxs-lookup"><span data-stu-id="c37f3-103">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from Windows Store apps is not supported</span></span>

## <a name="platforms"></a><span data-ttu-id="c37f3-104">平台</span><span class="sxs-lookup"><span data-stu-id="c37f3-104">Platforms</span></span>

<dl> <span data-ttu-id="c37f3-105">用戶端-windows 8。1</span><span class="sxs-lookup"><span data-stu-id="c37f3-105">Clients - windows 8.1</span></span>  
<span data-ttu-id="c37f3-106">伺服器-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c37f3-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="c37f3-107">描述</span><span class="sxs-lookup"><span data-stu-id="c37f3-107">Description</span></span>

<span data-ttu-id="c37f3-108">不支援從 Windows Store 應用程式呼叫 ImmSetConversionStatus () 或 ImmGetConversionStatus () ，而且可能會導致非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="c37f3-108">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from a Windows Store app is not supported and may cause unexpected results.</span></span>

## <a name="manifestations"></a><span data-ttu-id="c37f3-109">表現</span><span class="sxs-lookup"><span data-stu-id="c37f3-109">Manifestations</span></span>

<span data-ttu-id="c37f3-110">在應用程式啟動時，IME 模式會設定為下列預設值：</span><span class="sxs-lookup"><span data-stu-id="c37f3-110">At application start up, the IME mode is set to the following defaults:</span></span>



| &nbsp;   | <span data-ttu-id="c37f3-111">軟體輸入面板</span><span class="sxs-lookup"><span data-stu-id="c37f3-111">Software input panel</span></span> | <span data-ttu-id="c37f3-112">硬體鍵盤</span><span class="sxs-lookup"><span data-stu-id="c37f3-112">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="c37f3-113">KOR、JPN</span><span class="sxs-lookup"><span data-stu-id="c37f3-113">KOR, JPN</span></span> | <span data-ttu-id="c37f3-114">開啟</span><span class="sxs-lookup"><span data-stu-id="c37f3-114">On</span></span>                   | <span data-ttu-id="c37f3-115">關閉</span><span class="sxs-lookup"><span data-stu-id="c37f3-115">Off</span></span>               |
| <span data-ttu-id="c37f3-116">CHS、CHT</span><span class="sxs-lookup"><span data-stu-id="c37f3-116">CHS, CHT</span></span> | <span data-ttu-id="c37f3-117">開啟</span><span class="sxs-lookup"><span data-stu-id="c37f3-117">On</span></span>                   | <span data-ttu-id="c37f3-118">開啟</span><span class="sxs-lookup"><span data-stu-id="c37f3-118">On</span></span>                |



 

## <a name="solution"></a><span data-ttu-id="c37f3-119">解決方法</span><span class="sxs-lookup"><span data-stu-id="c37f3-119">Solution</span></span>

<span data-ttu-id="c37f3-120">開發人員可以藉由指定欄位的輸入範圍值，來控制預設的 IME 模式。</span><span class="sxs-lookup"><span data-stu-id="c37f3-120">Developers can control the default IME mode by specifying an input scope value for the field.</span></span>

<span data-ttu-id="c37f3-121">指定輸入範圍的輸入法模式取決於每個 IME。</span><span class="sxs-lookup"><span data-stu-id="c37f3-121">The IME mode for a specified input scope is determined by each IME.</span></span> <span data-ttu-id="c37f3-122">開發人員無法指定 IME 模式。</span><span class="sxs-lookup"><span data-stu-id="c37f3-122">Developers cannot specify the IME mode.</span></span>

## <a name="resources"></a><span data-ttu-id="c37f3-123">資源</span><span class="sxs-lookup"><span data-stu-id="c37f3-123">Resources</span></span>

-   [<span data-ttu-id="c37f3-124">InputScope 列舉</span><span class="sxs-lookup"><span data-stu-id="c37f3-124">InputScope Enumeration</span></span>](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [<span data-ttu-id="c37f3-125">ImmSetConversionStatus</span><span class="sxs-lookup"><span data-stu-id="c37f3-125">ImmSetConversionStatus</span></span>](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   <span data-ttu-id="c37f3-126">[ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="c37f3-126">[ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))</span></span>

 

 