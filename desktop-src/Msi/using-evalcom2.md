---
description: Evalcom2.dll 可以用來利用內部一致性評估工具來執行安裝套件和合併模組的驗證作業。
ms.assetid: df38e75e-554c-4a6d-b9ad-8eee5123a16f
title: 使用 Evalcom2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c49a165115b505d5c78ebe5b5e714b8a3c359d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690524"
---
# <a name="using-evalcom2"></a><span data-ttu-id="3fe3f-103">使用 Evalcom2</span><span class="sxs-lookup"><span data-stu-id="3fe3f-103">Using Evalcom2</span></span>

<span data-ttu-id="3fe3f-104">Evalcom2.dll 可以用來利用 [內部一致性評估](internal-consistency-evaluators-ices.md)工具來執行安裝套件和合併模組的驗證作業。</span><span class="sxs-lookup"><span data-stu-id="3fe3f-104">Evalcom2.dll can be used to implement validation operations for installation packages and merge modules using [Internal Consistency Evaluators - ICEs](internal-consistency-evaluators-ices.md).</span></span> <span data-ttu-id="3fe3f-105">主要物件會執行 C/c + + 程式的介面。</span><span class="sxs-lookup"><span data-stu-id="3fe3f-105">The main object implements interfaces for C/C++ programs.</span></span>

<span data-ttu-id="3fe3f-106">主要物件也會針對 C/c + + 程式執行 [Evalcom2 介面](evalcom2-interfaces.md) 。</span><span class="sxs-lookup"><span data-stu-id="3fe3f-106">The main object also implements [Evalcom2 interfaces](evalcom2-interfaces.md) for C/C++ programs.</span></span> <span data-ttu-id="3fe3f-107">從 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 取得介面所需的 CLSID 為 {6E5E1910-8053-4660-B795-6B612E29BC58}。</span><span class="sxs-lookup"><span data-stu-id="3fe3f-107">The CLSID required to obtain the interface from [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) is {6E5E1910-8053-4660-B795-6B612E29BC58}.</span></span> <span data-ttu-id="3fe3f-108">REFIID 是 {E482E5C6-E31E-4143-A2E6-DBC3D8E4B8D3}。</span><span class="sxs-lookup"><span data-stu-id="3fe3f-108">The REFIID is {E482E5C6-E31E-4143-A2E6-DBC3D8E4B8D3}.</span></span>

<span data-ttu-id="3fe3f-109">您可以使用下列程式來執行驗證作業。</span><span class="sxs-lookup"><span data-stu-id="3fe3f-109">You can use the following procedure to implement validation operations.</span></span>

<span data-ttu-id="3fe3f-110">**若要執行驗證作業**</span><span class="sxs-lookup"><span data-stu-id="3fe3f-110">**To implement validation operations**</span></span>

1.  <span data-ttu-id="3fe3f-111">使用 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize)初始化呼叫執行緒上的 COM。</span><span class="sxs-lookup"><span data-stu-id="3fe3f-111">Initialize COM on the calling thread using [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).</span></span>
2.  <span data-ttu-id="3fe3f-112">使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)取得 [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="3fe3f-112">Obtain the pointer to the [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) interface using [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>
3.  <span data-ttu-id="3fe3f-113">使用 [**OpenDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opendatabase) 方法開啟安裝封裝或合併模組。</span><span class="sxs-lookup"><span data-stu-id="3fe3f-113">Open the installation package or merge module using the [**OpenDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opendatabase) method.</span></span>
4.  <span data-ttu-id="3fe3f-114">使用 [**OpenCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub) 方法開啟評估檔案。</span><span class="sxs-lookup"><span data-stu-id="3fe3f-114">Open the evaluation file using the [**OpenCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub) method.</span></span>
5.  <span data-ttu-id="3fe3f-115">使用 [**SetDisplay**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay) 方法來設定顯示回撥函式。</span><span class="sxs-lookup"><span data-stu-id="3fe3f-115">Set the display callback function using the [**SetDisplay**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay) method.</span></span>
6.  <span data-ttu-id="3fe3f-116">使用 [**SetStatus**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus) 方法設定狀態回呼函數。</span><span class="sxs-lookup"><span data-stu-id="3fe3f-116">Set the status callback function using the [**SetStatus**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus) method.</span></span>
7.  <span data-ttu-id="3fe3f-117">使用 [**Validate**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-validate) 方法來執行驗證。</span><span class="sxs-lookup"><span data-stu-id="3fe3f-117">Perform the validation using the [**Validate**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-validate) method.</span></span>
8.  <span data-ttu-id="3fe3f-118">使用 [**CloseCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closecub) 方法來關閉 .cub 檔。</span><span class="sxs-lookup"><span data-stu-id="3fe3f-118">Close the .cub file using the [**CloseCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closecub) method.</span></span>
9.  <span data-ttu-id="3fe3f-119">使用 [**CloseDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closedatabase) 方法來關閉資料庫。</span><span class="sxs-lookup"><span data-stu-id="3fe3f-119">Close the database using the [**CloseDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closedatabase) method.</span></span>
10. <span data-ttu-id="3fe3f-120">釋放 [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) 介面。</span><span class="sxs-lookup"><span data-stu-id="3fe3f-120">Release the [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) interface.</span></span>
11. <span data-ttu-id="3fe3f-121">使用 [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)將 COM 解除初始化。</span><span class="sxs-lookup"><span data-stu-id="3fe3f-121">Uninitialize COM using [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fe3f-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="3fe3f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fe3f-123">Evalcom2 介面</span><span class="sxs-lookup"><span data-stu-id="3fe3f-123">Evalcom2 Interfaces</span></span>](evalcom2-interfaces.md)
</dt> <dt>

[<span data-ttu-id="3fe3f-124">驗證自動化</span><span class="sxs-lookup"><span data-stu-id="3fe3f-124">Validation Automation</span></span>](validation-automation.md)
</dt> <dt>

[<span data-ttu-id="3fe3f-125">驗證回呼函數</span><span class="sxs-lookup"><span data-stu-id="3fe3f-125">Validation Callback Functions</span></span>](validation-callback-functions.md)
</dt> </dl>

 

 
