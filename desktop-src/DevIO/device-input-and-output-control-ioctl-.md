---
description: DeviceIoControl 函式會提供裝置輸入和輸出控制項 (IOCTL) 介面，讓應用程式可以直接與設備磁碟機進行通訊。
ms.assetid: 2dffd86a-162c-4e09-bfa1-73b87522741a
title: " (IOCTL) 的裝置輸入和輸出控制項"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2bb2ee26c63c2aad02d8e8d167ff12383fc6b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847475"
---
# <a name="device-input-and-output-control-ioctl"></a><span data-ttu-id="35e3a-103"> (IOCTL) 的裝置輸入和輸出控制項</span><span class="sxs-lookup"><span data-stu-id="35e3a-103">Device Input and Output Control (IOCTL)</span></span>

<span data-ttu-id="35e3a-104">[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)函式會提供裝置輸入和輸出控制項 (IOCTL) 介面，讓應用程式可以直接與設備磁碟機進行通訊。</span><span class="sxs-lookup"><span data-stu-id="35e3a-104">The [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function provides a device input and output control (IOCTL) interface through which an application can communicate directly with a device driver.</span></span> <span data-ttu-id="35e3a-105">**DeviceIoControl** 函式是一般用途的介面，可將控制程式代碼傳送至各種裝置。</span><span class="sxs-lookup"><span data-stu-id="35e3a-105">The **DeviceIoControl** function is a general-purpose interface that can send control codes to a variety of devices.</span></span> <span data-ttu-id="35e3a-106">每個控制項程式碼代表驅動程式要執行的作業。</span><span class="sxs-lookup"><span data-stu-id="35e3a-106">Each control code represents an operation for the driver to perform.</span></span> <span data-ttu-id="35e3a-107">例如，控制程式代碼可以要求設備磁碟機傳回對應裝置的相關資訊，或指示驅動程式在裝置上執行動作，例如將磁片格式化。</span><span class="sxs-lookup"><span data-stu-id="35e3a-107">For example, a control code can ask a device driver to return information about the corresponding device, or direct the driver to carry out an action on the device, such as formatting a disk.</span></span>

<span data-ttu-id="35e3a-108">SDK 標頭檔中會定義一些標準控制項碼。</span><span class="sxs-lookup"><span data-stu-id="35e3a-108">A number of standard control codes are defined in the SDK header files.</span></span> <span data-ttu-id="35e3a-109">此外，設備磁碟機還可以定義自己的裝置特定控制項碼。</span><span class="sxs-lookup"><span data-stu-id="35e3a-109">In addition, device drivers can define their own device-specific control codes.</span></span> <span data-ttu-id="35e3a-110">如需 SDK 檔中包含的標準控制代碼清單，請參閱 [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)的「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="35e3a-110">For a list of standard control codes included in the SDK documentation, see the Remarks section of [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol).</span></span>

<span data-ttu-id="35e3a-111">您可以指定的控制程式代碼類型取決於正在存取的裝置，以及您的應用程式執行所在的平臺。</span><span class="sxs-lookup"><span data-stu-id="35e3a-111">The types of control codes you can specify depend on the device being accessed and the platform on which your application is running.</span></span> <span data-ttu-id="35e3a-112">應用程式可以使用標準控制代碼或裝置特定的控制碼，在磁片磁碟機、硬碟、磁帶機或 CD-ROM 光碟機上執行直接輸入和輸出作業。</span><span class="sxs-lookup"><span data-stu-id="35e3a-112">Applications can use the standard control codes or device-specific control codes to perform direct input and output operations on a floppy disk drive, hard disk drive, tape drive, or CD-ROM drive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35e3a-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="35e3a-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35e3a-114">呼叫 DeviceIoControl</span><span class="sxs-lookup"><span data-stu-id="35e3a-114">Calling DeviceIoControl</span></span>](calling-deviceiocontrol.md)
</dt> </dl>

 

 
