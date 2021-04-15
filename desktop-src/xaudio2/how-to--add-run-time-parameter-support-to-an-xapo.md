---
description: 您可以藉由執行 IXAPOParameters 介面，將執行時間參數支援新增至 XAPO。 執行時間參數支援可讓 XAPO 根據在執行時間傳遞給它的參數來變更其行為。
ms.assetid: 13f974ec-fcf5-1749-e69d-88de79b7d82b
title: 使用方法：新增 XAPO 的執行階段參數支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582f51b3dfbdc6d31422494906d5f945f77ccb03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469176"
---
# <a name="how-to-add-run-time-parameter-support-to-an-xapo"></a><span data-ttu-id="28ce4-104">使用方法：新增 XAPO 的執行階段參數支援</span><span class="sxs-lookup"><span data-stu-id="28ce4-104">How to: Add Run-time Parameter Support to an XAPO</span></span>

<span data-ttu-id="28ce4-105">您可以藉由執行 [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) 介面，將執行時間參數支援新增至 XAPO。</span><span class="sxs-lookup"><span data-stu-id="28ce4-105">You can add run-time parameter support to an XAPO by implementing the [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) interface.</span></span> <span data-ttu-id="28ce4-106">執行時間參數支援可讓 XAPO 根據在執行時間傳遞給它的參數來變更其行為。</span><span class="sxs-lookup"><span data-stu-id="28ce4-106">Run-time parameter support allows an XAPO to change its behavior based on the parameters passed to it at run time.</span></span>

1.  <span data-ttu-id="28ce4-107">遵循 how [to：建立 XAPO](how-to--create-an-xapo.md)中的步驟。</span><span class="sxs-lookup"><span data-stu-id="28ce4-107">Follow the steps in [How to: Create an XAPO](how-to--create-an-xapo.md).</span></span>
2.  <span data-ttu-id="28ce4-108">將 XAPO 變更為衍生自 [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) 和 [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase)。</span><span class="sxs-lookup"><span data-stu-id="28ce4-108">Change the XAPO to derive from [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) and [**CXAPOBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase).</span></span>
3.  <span data-ttu-id="28ce4-109">將 [**CXAPOParametersBase：： BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) 和 [**CXAPOParametersBase：： EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) 方法的呼叫新增至 [**IXAPO：:P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)的執行。</span><span class="sxs-lookup"><span data-stu-id="28ce4-109">Add calls to the methods [**CXAPOParametersBase::BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) and [**CXAPOParametersBase::EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) to the implementation of [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process).</span></span>

    > [!Note]  
    > <span data-ttu-id="28ce4-110">將這些方法加入至 [IXAPO：:P rocess](how-to--build-a-basic-audio-processing-graph.md) 可讓 [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) 將其效果參數的複本保存在安全線程狀態中。</span><span class="sxs-lookup"><span data-stu-id="28ce4-110">Adding these methods to [IXAPO::Process](how-to--build-a-basic-audio-processing-graph.md) allows [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) to keep its copies of the effect parameters in a thread-safe state.</span></span> <span data-ttu-id="28ce4-111">在 CXAPOParametersBase 的開頭呼叫 [**CXAPOParametersBase：： BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) （在 [**IXAPO：:P Rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)）和 [**EndProcess：： IXAPO**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) **：:P rocess**。</span><span class="sxs-lookup"><span data-stu-id="28ce4-111">Call [**CXAPOParametersBase::BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess) at the beginning of [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process), and [**CXAPOParametersBase::EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess) at the end of **IXAPO::Process**.</span></span>

     

4.  <span data-ttu-id="28ce4-112">將更多程式碼新增至 [**IXAPO：:P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) 執行，根據 [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) 方法所儲存的值來變更其行為。</span><span class="sxs-lookup"><span data-stu-id="28ce4-112">Add more code to the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) implementation to change its behavior according to values stored by the [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) method.</span></span>

    > [!Note]  
    > <span data-ttu-id="28ce4-113">將程式碼加入至 [**IXAPO：:P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) 方法以使用 [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) 指定的參數，可讓 XAPO 的行為在整個生命週期中變更。</span><span class="sxs-lookup"><span data-stu-id="28ce4-113">Adding code to the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) method to use the parameters specified by [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) allows the XAPO's behavior to be changed throughout its life.</span></span>

     

5.  <span data-ttu-id="28ce4-114">當您建立效果的實例時，請配置三個結構的緩衝區以表示效果的參數，並將其傳遞至 [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) 的函式。</span><span class="sxs-lookup"><span data-stu-id="28ce4-114">When you create an instance of the effect, allocate a buffer of three of the structures that will represent the effect's parameters, and pass it to the [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) constructor.</span></span>

    > [!Note]  
    > <span data-ttu-id="28ce4-115">當您呼叫 [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters)時， [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase)實例會在內部使用這個緩衝區來管理傳遞給它的效果參數。</span><span class="sxs-lookup"><span data-stu-id="28ce4-115">The [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) instance internally uses this buffer to manage effect parameters passed to it when you call [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters).</span></span> <span data-ttu-id="28ce4-116">您必須在呼叫任何 [**IXAPO：:P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process)、 [**IXAPOParameters：： GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters)和 **IXAPOParameters：： SetParameters** 方法之前，將 *pParameterBlocks* 中的所有流程參數區塊初始化為相同的預設值。</span><span class="sxs-lookup"><span data-stu-id="28ce4-116">You must initialize all the process parameter blocks in *pParameterBlocks* to the same default value before you call any of the [**IXAPO::Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process), [**IXAPOParameters::GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters), and **IXAPOParameters::SetParameters** methods.</span></span> <span data-ttu-id="28ce4-117">此初始化通常會在 [**IXAPO：： Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) 或 [**IXAPO：： LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess)中處理。</span><span class="sxs-lookup"><span data-stu-id="28ce4-117">Usually this initialization is handled in [**IXAPO::Initialize**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) or in [**IXAPO::LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess).</span></span>

     

## <a name="related-topics"></a><span data-ttu-id="28ce4-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="28ce4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28ce4-119">音訊效果</span><span class="sxs-lookup"><span data-stu-id="28ce4-119">Audio Effects</span></span>](audio-effects.md)
</dt> <dt>

[<span data-ttu-id="28ce4-120">XAPO 概觀</span><span class="sxs-lookup"><span data-stu-id="28ce4-120">XAPO Overview</span></span>](xapo-overview.md)
</dt> </dl>

 

 
