---
title: JAVA 和 Visual Basic 中的 COM 錯誤處理
description: JAVA 和 Visual Basic 中的 COM 錯誤處理
ms.assetid: 1130a038-3c18-4530-a6d7-9f538352297f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea12dc040218e14098ce2394fbb5cd2ebeff1704
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382962"
---
# <a name="com-error-handling-in-java-and-visual-basic"></a><span data-ttu-id="2c064-103">JAVA 和 Visual Basic 中的 COM 錯誤處理</span><span class="sxs-lookup"><span data-stu-id="2c064-103">COM Error Handling in Java and Visual Basic</span></span>

<span data-ttu-id="2c064-104">在 JAVA 或 Microsoft Visual Basic 中進行程式設計時，可在 COM 中使用三個介面和三個函式來提供錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="2c064-104">There are three interfaces and three functions that can be used in COM to provide error handling when programming in Java or Microsoft Visual Basic.</span></span> <span data-ttu-id="2c064-105">在 JAVA 和 Visual Basic 中，方法呼叫不會傳回 **HRESULT** 作為傳回值。</span><span class="sxs-lookup"><span data-stu-id="2c064-105">In Java and Visual Basic, the method call does not return an **HRESULT** as the return value.</span></span> <span data-ttu-id="2c064-106">相反地，這些語言會使用 COM 介面和函式來取得 **HRESULT** 值，以及處理錯誤或例外狀況。</span><span class="sxs-lookup"><span data-stu-id="2c064-106">Instead, these languages use the COM interfaces and functions to obtain **HRESULT** values and to handle errors or exceptions.</span></span> <span data-ttu-id="2c064-107"> (例外狀況是程式控制項以外的事件，例如檔案問題或不正確參數。 ) </span><span class="sxs-lookup"><span data-stu-id="2c064-107">(Exceptions are events beyond the program's control, such as file problems or invalid parameters.)</span></span>

<span data-ttu-id="2c064-108">下表將列出提供 **HRESULT** 支援的三個介面，並簡短說明。</span><span class="sxs-lookup"><span data-stu-id="2c064-108">The three interfaces that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|                                                                          |                                                                                                                      |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c064-109">**ICreateErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="2c064-109">**ICreateErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)<br/>  | <span data-ttu-id="2c064-110">設定錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="2c064-110">Sets error information.</span></span><br/>                                                                                   |
| [<span data-ttu-id="2c064-111">**IErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="2c064-111">**IErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>        | <span data-ttu-id="2c064-112">從錯誤物件傳回信息。</span><span class="sxs-lookup"><span data-stu-id="2c064-112">Returns information from an error object.</span></span><br/>                                                                 |
| [<span data-ttu-id="2c064-113">**ISupportErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="2c064-113">**ISupportErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)<br/> | <span data-ttu-id="2c064-114">將物件識別為支援 [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) 介面。</span><span class="sxs-lookup"><span data-stu-id="2c064-114">Identifies the object as supporting the [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) interface.</span></span><br/> |



 

<span data-ttu-id="2c064-115">提供 **HRESULT** 的支援的三個函式會在下表中列出並簡短說明。</span><span class="sxs-lookup"><span data-stu-id="2c064-115">The three functions that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|                                                                        |                                                                                                                                                                      |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c064-116">**CreateErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="2c064-116">**CreateErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)<br/> | <span data-ttu-id="2c064-117">建立泛型錯誤物件的實例。</span><span class="sxs-lookup"><span data-stu-id="2c064-117">Creates an instance of a generic error object.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="2c064-118">**GetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="2c064-118">**GetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)<br/>    | <span data-ttu-id="2c064-119">取得上一次呼叫目前邏輯執行緒中的 [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) 所設定的錯誤資訊指標。</span><span class="sxs-lookup"><span data-stu-id="2c064-119">Obtains the error information pointer set by the previous call to [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) in the current logical thread.</span></span><br/> |
| [<span data-ttu-id="2c064-120">**SetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="2c064-120">**SetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)<br/>    | <span data-ttu-id="2c064-121">為目前執行中的執行緒設定錯誤資訊物件。</span><span class="sxs-lookup"><span data-stu-id="2c064-121">Sets the error information object for the current thread of execution.</span></span><br/>                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="2c064-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="2c064-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c064-123">COM 中的錯誤處理</span><span class="sxs-lookup"><span data-stu-id="2c064-123">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

