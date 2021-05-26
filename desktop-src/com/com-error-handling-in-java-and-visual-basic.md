---
title: JAVA 和 Visual Basic 中的 COM 錯誤處理
description: JAVA 和 Visual Basic 中的 COM 錯誤處理
ms.assetid: 1130a038-3c18-4530-a6d7-9f538352297f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c55c1c2414c69ff9398845858baadebd58cbf9
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424008"
---
# <a name="com-error-handling-in-java-and-visual-basic"></a><span data-ttu-id="a2ac6-103">JAVA 和 Visual Basic 中的 COM 錯誤處理</span><span class="sxs-lookup"><span data-stu-id="a2ac6-103">COM Error Handling in Java and Visual Basic</span></span>

<span data-ttu-id="a2ac6-104">在 JAVA 或 Microsoft Visual Basic 中進行程式設計時，可在 COM 中使用三個介面和三個函式來提供錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="a2ac6-104">There are three interfaces and three functions that can be used in COM to provide error handling when programming in Java or Microsoft Visual Basic.</span></span> <span data-ttu-id="a2ac6-105">在 JAVA 和 Visual Basic 中，方法呼叫不會傳回 **HRESULT** 作為傳回值。</span><span class="sxs-lookup"><span data-stu-id="a2ac6-105">In Java and Visual Basic, the method call does not return an **HRESULT** as the return value.</span></span> <span data-ttu-id="a2ac6-106">相反地，這些語言會使用 COM 介面和函式來取得 **HRESULT** 值，以及處理錯誤或例外狀況。</span><span class="sxs-lookup"><span data-stu-id="a2ac6-106">Instead, these languages use the COM interfaces and functions to obtain **HRESULT** values and to handle errors or exceptions.</span></span> <span data-ttu-id="a2ac6-107"> (例外狀況是程式控制項以外的事件，例如檔案問題或不正確參數。 ) </span><span class="sxs-lookup"><span data-stu-id="a2ac6-107">(Exceptions are events beyond the program's control, such as file problems or invalid parameters.)</span></span>

<span data-ttu-id="a2ac6-108">下表將列出提供 **HRESULT** 支援的三個介面，並簡短說明。</span><span class="sxs-lookup"><span data-stu-id="a2ac6-108">The three interfaces that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|  <span data-ttu-id="a2ac6-109">介面</span><span class="sxs-lookup"><span data-stu-id="a2ac6-109">Interface</span></span>                                                                        |  <span data-ttu-id="a2ac6-110">描述</span><span class="sxs-lookup"><span data-stu-id="a2ac6-110">Description</span></span>                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2ac6-111">**ICreateErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="a2ac6-111">**ICreateErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)<br/>  | <span data-ttu-id="a2ac6-112">設定錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="a2ac6-112">Sets error information.</span></span><br/>                                                                                   |
| [<span data-ttu-id="a2ac6-113">**IErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="a2ac6-113">**IErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>        | <span data-ttu-id="a2ac6-114">從錯誤物件傳回信息。</span><span class="sxs-lookup"><span data-stu-id="a2ac6-114">Returns information from an error object.</span></span><br/>                                                                 |
| [<span data-ttu-id="a2ac6-115">**ISupportErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="a2ac6-115">**ISupportErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)<br/> | <span data-ttu-id="a2ac6-116">將物件識別為支援 [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) 介面。</span><span class="sxs-lookup"><span data-stu-id="a2ac6-116">Identifies the object as supporting the [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) interface.</span></span><br/> |



 

<span data-ttu-id="a2ac6-117">提供 **HRESULT** 的支援的三個函式會在下表中列出並簡短說明。</span><span class="sxs-lookup"><span data-stu-id="a2ac6-117">The three functions that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|    <span data-ttu-id="a2ac6-118">介面</span><span class="sxs-lookup"><span data-stu-id="a2ac6-118">Interface</span></span>       |       <span data-ttu-id="a2ac6-119">描述</span><span class="sxs-lookup"><span data-stu-id="a2ac6-119">Description</span></span>       |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2ac6-120">**CreateErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="a2ac6-120">**CreateErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)<br/> | <span data-ttu-id="a2ac6-121">建立泛型錯誤物件的實例。</span><span class="sxs-lookup"><span data-stu-id="a2ac6-121">Creates an instance of a generic error object.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="a2ac6-122">**GetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="a2ac6-122">**GetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)<br/>    | <span data-ttu-id="a2ac6-123">取得上一次呼叫目前邏輯執行緒中的 [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) 所設定的錯誤資訊指標。</span><span class="sxs-lookup"><span data-stu-id="a2ac6-123">Obtains the error information pointer set by the previous call to [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) in the current logical thread.</span></span><br/> |
| [<span data-ttu-id="a2ac6-124">**SetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="a2ac6-124">**SetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)<br/>    | <span data-ttu-id="a2ac6-125">為目前執行中的執行緒設定錯誤資訊物件。</span><span class="sxs-lookup"><span data-stu-id="a2ac6-125">Sets the error information object for the current thread of execution.</span></span><br/>                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="a2ac6-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="a2ac6-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2ac6-127">COM 中的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="a2ac6-127">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

