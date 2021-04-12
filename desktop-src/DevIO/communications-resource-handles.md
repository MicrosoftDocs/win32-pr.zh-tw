---
description: 進程會使用 CreateFile 函式來開啟通訊資源的控制碼。
ms.assetid: eaef6067-97a6-40c4-84ec-c0d86af6bb4a
title: 通訊資源控制碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709fc041f6125d93a1c52f3e17b77c96f35825c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385938"
---
# <a name="communications-resource-handles"></a><span data-ttu-id="b5968-103">通訊資源控制碼</span><span class="sxs-lookup"><span data-stu-id="b5968-103">Communications Resource Handles</span></span>

<span data-ttu-id="b5968-104">進程會使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 函式來開啟通訊資源的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b5968-104">A process uses the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open a handle to a communications resource.</span></span> <span data-ttu-id="b5968-105">例如，指定 COM1 會開啟序列埠的控制碼，而 LPT1 會開啟平行埠的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b5968-105">For example, specifying COM1 opens a handle to a serial port, and LPT1 opens a handle to a parallel port.</span></span> <span data-ttu-id="b5968-106">如果指定的資源目前正由另一個進程使用中， **CreateFile** 就會失敗。</span><span class="sxs-lookup"><span data-stu-id="b5968-106">If the specified resource is currently being used by another process, **CreateFile** fails.</span></span> <span data-ttu-id="b5968-107">進程的任何執行緒都可以使用 **CreateFile** 所傳回的控制碼，來識別存取資源之任何函式中的資源。</span><span class="sxs-lookup"><span data-stu-id="b5968-107">Any thread of the process can use the handle returned by **CreateFile** to identify the resource in any of the functions that access the resource.</span></span>

<span data-ttu-id="b5968-108">當進程呼叫 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 開啟通訊資源時，它會指定下列屬性：</span><span class="sxs-lookup"><span data-stu-id="b5968-108">When the process calls [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open a communications resource, it specifies the following attributes:</span></span>

-   <span data-ttu-id="b5968-109">指定資源存在何種類型的讀取/寫入存取權。</span><span class="sxs-lookup"><span data-stu-id="b5968-109">What type of read/write access exists for the specified resource.</span></span>
-   <span data-ttu-id="b5968-110">控制碼是否可由子進程繼承。</span><span class="sxs-lookup"><span data-stu-id="b5968-110">Whether the handle can be inherited by child processes.</span></span>
-   <span data-ttu-id="b5968-111">控制碼是否可用於重迭 (非同步) i/o 作業。</span><span class="sxs-lookup"><span data-stu-id="b5968-111">Whether the handle can be used in overlapped (asynchronous) I/O operations.</span></span> <span data-ttu-id="b5968-112"> (如需重迭作業的描述，請參閱 [同步](/windows/desktop/Sync/synchronization)處理。 ) </span><span class="sxs-lookup"><span data-stu-id="b5968-112">(For a description of overlapped operations, see [Synchronization](/windows/desktop/Sync/synchronization).)</span></span>

<span data-ttu-id="b5968-113">當程式使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) 開啟通訊資源時，它必須指定下列參數的特定值：</span><span class="sxs-lookup"><span data-stu-id="b5968-113">When the process uses [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open a communications resource, it must specify certain values for the following parameters:</span></span>

-   <span data-ttu-id="b5968-114">*FdwShareMode* 參數必須為零，開啟資源以進行獨佔存取。</span><span class="sxs-lookup"><span data-stu-id="b5968-114">The *fdwShareMode* parameter must be zero, opening the resource for exclusive access.</span></span>
-   <span data-ttu-id="b5968-115">*FdwCreate* 參數必須指定 OPEN \_ EXISTING 旗標。</span><span class="sxs-lookup"><span data-stu-id="b5968-115">The *fdwCreate* parameter must specify the OPEN\_EXISTING flag.</span></span>
-   <span data-ttu-id="b5968-116">*HTemplateFile* 參數必須為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b5968-116">The *hTemplateFile* parameter must be **NULL**.</span></span>

<span data-ttu-id="b5968-117">使用 [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)直接將控制碼開啟至裝置時，應用程式必須使用特殊字元 " \\ \\ . \\ " 來識別裝置。</span><span class="sxs-lookup"><span data-stu-id="b5968-117">When using [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open a handle directly to a device, an application must use the special characters " \\\\ .\\" to identify the device.</span></span> <span data-ttu-id="b5968-118">例如，若要開啟磁片磁碟機 A 的控制碼，請指定 \\ \\ 。 \\a：適用于 **CreateFile** 的 *lpszName* 參數。</span><span class="sxs-lookup"><span data-stu-id="b5968-118">For example, to open a handle to drive A, specify \\\\ .\\a: for the *lpszName* parameter of **CreateFile**.</span></span> <span data-ttu-id="b5968-119">呼叫進程可使用 [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) 函式中的控制碼，將控制程式代碼傳送至裝置。</span><span class="sxs-lookup"><span data-stu-id="b5968-119">The calling process can use the handle in the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function to send control codes to the device.</span></span>

 

 
