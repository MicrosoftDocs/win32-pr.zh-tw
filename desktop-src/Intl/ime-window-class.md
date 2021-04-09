---
description: IME 視窗類別是預先定義的系統全域類別，可定義標準 IME 視窗的外觀和行為。
ms.assetid: 0fa01d84-1304-4235-a148-ea5e8dd5d0b3
title: IME 視窗類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faae7fd0135ec894186b4e10df9bc02da66bb933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849482"
---
# <a name="ime-window-class"></a><span data-ttu-id="a2e36-103">IME 視窗類別</span><span class="sxs-lookup"><span data-stu-id="a2e36-103">IME Window Class</span></span>

<span data-ttu-id="a2e36-104">IME 視窗類別是預先定義的系統全域類別，可定義標準 IME 視窗的外觀和行為。</span><span class="sxs-lookup"><span data-stu-id="a2e36-104">The IME window class is a predefined system global class that defines the appearance and behavior of the standard IME windows.</span></span> <span data-ttu-id="a2e36-105">類別類似于通用控制項類別，因為應用程式會使用 [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) 函數來建立這個類別的視窗。</span><span class="sxs-lookup"><span data-stu-id="a2e36-105">The class is similar to common control classes in that the application creates a window of this class by using the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function.</span></span> <span data-ttu-id="a2e36-106">和靜態控制項一樣，IME 視窗本身不會回應使用者輸入。</span><span class="sxs-lookup"><span data-stu-id="a2e36-106">Like static controls, an IME window does not respond to user input by itself.</span></span> <span data-ttu-id="a2e36-107">相反地，它會通知使用者輸入動作的輸入法，並處理由 IME 或應用程式傳送給它的控制訊息，以執行使用者動作的回應。</span><span class="sxs-lookup"><span data-stu-id="a2e36-107">Instead, it notifies the IME of user input actions and processes control messages sent to it by the IME or applications to carry out a response to the user action.</span></span>

<span data-ttu-id="a2e36-108">IME 感知應用程式有時會使用 IME 視窗類別來建立自訂的 IME 視窗。</span><span class="sxs-lookup"><span data-stu-id="a2e36-108">IME-aware applications sometimes create customized IME windows using the IME window class.</span></span> <span data-ttu-id="a2e36-109">使用視窗自訂可讓應用程式利用 IME 視窗的預設處理，同時控制視窗定位。</span><span class="sxs-lookup"><span data-stu-id="a2e36-109">Use of window customization allows the application to take advantage of the default processing of the IME window while having control of window positioning.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a2e36-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="a2e36-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2e36-111">關於輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="a2e36-111">About Input Method Manager</span></span>](about-input-method-manager.md)
</dt> </dl>

 

 
