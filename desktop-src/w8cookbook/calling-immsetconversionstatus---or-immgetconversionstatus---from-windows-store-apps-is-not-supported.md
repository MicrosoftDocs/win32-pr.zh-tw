---
title: '不支援從 Windows Store 應用程式呼叫 ImmSetConversionStatus () 或 ImmGetConversionStatus () '
description: '不支援從 Windows Store 應用程式呼叫 ImmSetConversionStatus () 或 ImmGetConversionStatus () '
ms.assetid: C6F3C8E7-E07A-40C6-A257-037766C670E7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b0846b56b1d6c2367c46e4adf82dac011c49fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682456"
---
# <a name="calling-immsetconversionstatus-or-immgetconversionstatus-from-windows-store-apps-is-not-supported"></a><span data-ttu-id="0093e-103">不支援從 Windows Store 應用程式呼叫 ImmSetConversionStatus () 或 ImmGetConversionStatus () </span><span class="sxs-lookup"><span data-stu-id="0093e-103">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from Windows Store apps is not supported</span></span>

## <a name="platforms"></a><span data-ttu-id="0093e-104">平台</span><span class="sxs-lookup"><span data-stu-id="0093e-104">Platforms</span></span>

<dl> <span data-ttu-id="0093e-105">用戶端-windows 8。1</span><span class="sxs-lookup"><span data-stu-id="0093e-105">Clients - windows 8.1</span></span>  
<span data-ttu-id="0093e-106">伺服器-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0093e-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="0093e-107">Description</span><span class="sxs-lookup"><span data-stu-id="0093e-107">Description</span></span>

<span data-ttu-id="0093e-108">不支援從 Windows Store 應用程式呼叫 ImmSetConversionStatus () 或 ImmGetConversionStatus () ，而且可能會導致非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="0093e-108">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from a Windows Store app is not supported and may cause unexpected results.</span></span>

## <a name="manifestations"></a><span data-ttu-id="0093e-109">表現</span><span class="sxs-lookup"><span data-stu-id="0093e-109">Manifestations</span></span>

<span data-ttu-id="0093e-110">在應用程式啟動時，IME 模式會設定為下列預設值：</span><span class="sxs-lookup"><span data-stu-id="0093e-110">At application start up, the IME mode is set to the following defaults:</span></span>



|          | <span data-ttu-id="0093e-111">軟體輸入面板</span><span class="sxs-lookup"><span data-stu-id="0093e-111">Software input panel</span></span> | <span data-ttu-id="0093e-112">硬體鍵盤</span><span class="sxs-lookup"><span data-stu-id="0093e-112">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="0093e-113">KOR、JPN</span><span class="sxs-lookup"><span data-stu-id="0093e-113">KOR, JPN</span></span> | <span data-ttu-id="0093e-114">開啟</span><span class="sxs-lookup"><span data-stu-id="0093e-114">On</span></span>                   | <span data-ttu-id="0093e-115">關閉</span><span class="sxs-lookup"><span data-stu-id="0093e-115">Off</span></span>               |
| <span data-ttu-id="0093e-116">CHS、CHT</span><span class="sxs-lookup"><span data-stu-id="0093e-116">CHS, CHT</span></span> | <span data-ttu-id="0093e-117">開啟</span><span class="sxs-lookup"><span data-stu-id="0093e-117">On</span></span>                   | <span data-ttu-id="0093e-118">開啟</span><span class="sxs-lookup"><span data-stu-id="0093e-118">On</span></span>                |



 

## <a name="solution"></a><span data-ttu-id="0093e-119">解決方法</span><span class="sxs-lookup"><span data-stu-id="0093e-119">Solution</span></span>

<span data-ttu-id="0093e-120">開發人員可以藉由指定欄位的輸入範圍值，來控制預設的 IME 模式。</span><span class="sxs-lookup"><span data-stu-id="0093e-120">Developers can control the default IME mode by specifying an input scope value for the field.</span></span>

<span data-ttu-id="0093e-121">指定輸入範圍的輸入法模式取決於每個 IME。</span><span class="sxs-lookup"><span data-stu-id="0093e-121">The IME mode for a specified input scope is determined by each IME.</span></span> <span data-ttu-id="0093e-122">開發人員無法指定 IME 模式。</span><span class="sxs-lookup"><span data-stu-id="0093e-122">Developers cannot specify the IME mode.</span></span>

## <a name="resources"></a><span data-ttu-id="0093e-123">資源</span><span class="sxs-lookup"><span data-stu-id="0093e-123">Resources</span></span>

-   [<span data-ttu-id="0093e-124">InputScope 列舉</span><span class="sxs-lookup"><span data-stu-id="0093e-124">InputScope Enumeration</span></span>](/windows/win32/api/inputscope/ne-inputscope-inputscope)
-   [<span data-ttu-id="0093e-125">ImmSetConversionStatus</span><span class="sxs-lookup"><span data-stu-id="0093e-125">ImmSetConversionStatus</span></span>](/windows/win32/api/immdev/nf-immdev-immsetconversionstatus)
-   <span data-ttu-id="0093e-126">[ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="0093e-126">[ImmGetConversionStatus](/previous-versions/aa912903(v=msdn.10))</span></span>

 

 