---
title: 擷取錯誤資訊
description: 擷取錯誤資訊
ms.assetid: 51a0e401-43f2-4738-9799-a96e2580a29f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6a5918ee7338d1b8428079da20ecb43c7b4b4ef
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024123"
---
# <a name="retrieving-error-information"></a><span data-ttu-id="97d45-103">擷取錯誤資訊</span><span class="sxs-lookup"><span data-stu-id="97d45-103">Retrieving Error Information</span></span>

<span data-ttu-id="97d45-104">使用 COM 錯誤處理介面和函式時，您可以如下所示取得錯誤資訊：</span><span class="sxs-lookup"><span data-stu-id="97d45-104">Using the COM error-handling interfaces and functions, you can retrieve error information as follows:</span></span>

1.  <span data-ttu-id="97d45-105">檢查傳回的值是否代表物件已準備好處理的錯誤。</span><span class="sxs-lookup"><span data-stu-id="97d45-105">Check whether the returned value represents an error that the object is prepared to handle.</span></span>
2.  <span data-ttu-id="97d45-106">呼叫 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) 以取得 [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="97d45-106">Call [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) to get a pointer to the [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) interface.</span></span> <span data-ttu-id="97d45-107">然後呼叫 [**ISupportErrorInfo：： InterfaceSupportsErrorInfo**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) ，以確認此錯誤是由傳回它的物件所引發，而且錯誤物件與目前的錯誤相關，而不是先前的呼叫。</span><span class="sxs-lookup"><span data-stu-id="97d45-107">Then call [**ISupportErrorInfo::InterfaceSupportsErrorInfo**](/windows/win32/api/oaidl/nf-oaidl-isupporterrorinfo-interfacesupportserrorinfo) to verify that the error was raised by the object that returned it and that the error object pertains to the current error and not to a previous call.</span></span>
3.  <span data-ttu-id="97d45-108">若要取得錯誤物件的指標，請呼叫 [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="97d45-108">To get a pointer to the error object, call the [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) function.</span></span>
4.  <span data-ttu-id="97d45-109">若要從錯誤物件取出資訊，請使用 [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) 方法。</span><span class="sxs-lookup"><span data-stu-id="97d45-109">To retrieve information from the error object, use the [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) methods.</span></span>

<span data-ttu-id="97d45-110">如果物件未準備好處理錯誤，但需要將錯誤資訊向下傳播至呼叫鏈，則應該只將傳回值傳遞給它的呼叫端。</span><span class="sxs-lookup"><span data-stu-id="97d45-110">If the object is not prepared to handle the error but needs to propagate the error information further down the call chain, it should simply pass the return value to its caller.</span></span> <span data-ttu-id="97d45-111">因為 [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) 函式會清除錯誤資訊，並將錯誤物件的擁有權傳遞給呼叫者，所以函式只能由處理錯誤的物件呼叫。</span><span class="sxs-lookup"><span data-stu-id="97d45-111">Because the [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo) function clears the error information and passes ownership of the error object to the caller, the function should be called only by the object that handles the error.</span></span>

 

 