---
description: 使用 IME 感知應用程式中的 IMM 功能，可讓使用者不需要記住所有可能的字元值。
ms.assetid: 43b3e561-b844-4688-ab3d-d99f92ed140e
title: 關於輸入方法管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7b96c64eba5ddfb6966c96d88792fd657f94aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987229"
---
# <a name="about-input-method-manager"></a><span data-ttu-id="26ffb-103">關於輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="26ffb-103">About Input Method Manager</span></span>

<span data-ttu-id="26ffb-104">使用 IME 感知應用程式中的 IMM 功能，可讓使用者不需要記住所有可能的字元值。</span><span class="sxs-lookup"><span data-stu-id="26ffb-104">Use of the IMM functionality in your IME-aware application relieves users of the need to remember all possible character values.</span></span> <span data-ttu-id="26ffb-105">相反地，它會允許 IME 監視使用者的按鍵，並預期使用者可能想要的字元，並提供可供選擇的候選字元清單。</span><span class="sxs-lookup"><span data-stu-id="26ffb-105">Instead, it allows the IME to monitor a user's keystrokes, anticipates the characters the user might want, and presents a list of candidate characters from which to choose.</span></span>

> [!Note]  
> <span data-ttu-id="26ffb-106">在與文字服務通訊的應用程式所使用的 [文字服務架構](../tsf/text-services-framework.md)中，IMM 會執行類似的作業。</span><span class="sxs-lookup"><span data-stu-id="26ffb-106">The IMM performs similar operations to those of the [Text Services Framework](../tsf/text-services-framework.md), used by applications that communicate with text services.</span></span>

 

<span data-ttu-id="26ffb-107">根據預設，IMM 會提供 IME 視窗，使用者可透過此視窗輸入按鍵和流覽並選取候選項目。</span><span class="sxs-lookup"><span data-stu-id="26ffb-107">By default, the IMM provides an IME window through which the user enters keystrokes and views and selects candidates.</span></span> <span data-ttu-id="26ffb-108">應用程式可以使用 IMM 函式和訊息來建立和管理自己的 IME 視窗，並在使用 IME 的轉換功能時提供自訂介面。</span><span class="sxs-lookup"><span data-stu-id="26ffb-108">Applications can use the IMM functions and messages to create and manage their own IME windows, providing a custom interface while using the conversion capabilities of the IME.</span></span>

<span data-ttu-id="26ffb-109">只有在東亞 (中文、日文、韓文) 當地語系化的 Windows 作業系統上，才會啟用 IMM。</span><span class="sxs-lookup"><span data-stu-id="26ffb-109">The IMM is only enabled on East Asian (Chinese, Japanese, Korean) localized Windows operating systems.</span></span> <span data-ttu-id="26ffb-110">在這些系統中，應用程式會使用 SM DBCSENABLED 呼叫 [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) ， \_ 以判斷是否已啟用 IMM。</span><span class="sxs-lookup"><span data-stu-id="26ffb-110">On these systems, the application calls [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) with SM\_DBCSENABLED to determine if the IMM is enabled.</span></span>

<span data-ttu-id="26ffb-111">**Windows 2000：** 所有當地語系化的語言版本都提供完整功能的 IMM 支援。</span><span class="sxs-lookup"><span data-stu-id="26ffb-111">**Windows 2000:** Full-featured IMM support is provided in all localized language versions.</span></span> <span data-ttu-id="26ffb-112">不過，只有在安裝了亞洲語言套件時，才會啟用 IMM。</span><span class="sxs-lookup"><span data-stu-id="26ffb-112">However, the IMM is enabled only when an Asian language pack is installed.</span></span> <span data-ttu-id="26ffb-113">IME 感知的應用程式可以使用 SM IMMENABLED 呼叫 [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) \_ ，以判斷是否已啟用 IMM。</span><span class="sxs-lookup"><span data-stu-id="26ffb-113">An IME-aware application can call [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) with SM\_IMMENABLED to determine if the IMM is enabled.</span></span>

<span data-ttu-id="26ffb-114">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="26ffb-114">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="26ffb-115">候選清單</span><span class="sxs-lookup"><span data-stu-id="26ffb-115">Candidate Lists</span></span>](candidate-lists.md)
-   [<span data-ttu-id="26ffb-116">組合字元串</span><span class="sxs-lookup"><span data-stu-id="26ffb-116">Composition String</span></span>](composition-string.md)
-   [<span data-ttu-id="26ffb-117">HexToUnicode IME</span><span class="sxs-lookup"><span data-stu-id="26ffb-117">HexToUnicode IME</span></span>](hextounicode-ime.md)
-   [<span data-ttu-id="26ffb-118">快速鍵</span><span class="sxs-lookup"><span data-stu-id="26ffb-118">Hot Keys</span></span>](hot-keys.md)
-   [<span data-ttu-id="26ffb-119">輸入法訊息</span><span class="sxs-lookup"><span data-stu-id="26ffb-119">IME Messages</span></span>](ime-messages.md)
-   [<span data-ttu-id="26ffb-120">IME 視窗類別</span><span class="sxs-lookup"><span data-stu-id="26ffb-120">IME Window Class</span></span>](ime-window-class.md)
-   [<span data-ttu-id="26ffb-121">輸入內容</span><span class="sxs-lookup"><span data-stu-id="26ffb-121">Input Context</span></span>](input-context.md)
-   [<span data-ttu-id="26ffb-122">狀態、撰寫和候選視窗</span><span class="sxs-lookup"><span data-stu-id="26ffb-122">Status, Composition, and Candidates Windows</span></span>](status--composition--and-candidates-windows.md)

 

 
