---
description: 應用程式內容可以用來建立並存的 Windows 類別。
ms.assetid: 4941ae1b-f9c6-45ff-b39b-a4078a12a58c
title: 建立並存的 Windows 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161732522a12fb6924a2850031d77cff53e44eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849907"
---
# <a name="creating-side-by-side-windows-classes"></a><span data-ttu-id="fe651-103">建立並存的 Windows 類別</span><span class="sxs-lookup"><span data-stu-id="fe651-103">Creating Side-By-Side Windows Classes</span></span>

<span data-ttu-id="fe651-104">應用程式內容可以用來建立並存的 Windows 類別。</span><span class="sxs-lookup"><span data-stu-id="fe651-104">Application contexts can be used to create side-by-side Windows classes.</span></span> <span data-ttu-id="fe651-105">藉由使用並存的 Windows 類別，您的應用程式可以在獨立的父視窗中同時有不同版本的可用類別。</span><span class="sxs-lookup"><span data-stu-id="fe651-105">By using side-by-side Windows classes, your application can have different versions of a class active at the same time in a lone parent window.</span></span> <span data-ttu-id="fe651-106">若要建立並存的 Windows 類別，您的應用程式必須先啟用啟用內容，然後再呼叫 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 來取得新視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fe651-106">To create a side-by-side Windows class, your application must activate an activation context before calling [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to obtain a handle to the new window.</span></span>

<span data-ttu-id="fe651-107">例如，Windows 通用控制項5.82 版和6.0 版都有編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="fe651-107">For example, Windows Common Controls version 5.82 and version 6.0 both had an Edit control.</span></span> <span data-ttu-id="fe651-108">Windows 預設為使用5.82 版編輯控制項。</span><span class="sxs-lookup"><span data-stu-id="fe651-108">Windows defaults to using the version 5.82 Edit control.</span></span> <span data-ttu-id="fe651-109">若要取得具有版本6.0 編輯控制項的並列視窗，在正常呼叫 [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) 之前，您的應用程式可以參考公開命名視窗類別的元件，然後啟動參考6.0 版控制項的啟用內容。</span><span class="sxs-lookup"><span data-stu-id="fe651-109">To obtain a side-by-side window that has the version 6.0 Edit control, before calling [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) as usual, your application can reference an assembly that exposes named window classes and then activate the activation context that references the version 6.0 controls.</span></span>

 

 
