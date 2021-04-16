---
description: 如果應用程式要求隨機鎖定，則必須使用 CreateFile 函式搭配檔案旗標重迭旗標，開啟其要求鎖定的所有檔案，以便重迭 (非同步) 輸入和輸出 \_ \_ 。
ms.assetid: 1595c03e-9f6d-456c-8164-fafba06bbd79
title: 隨機鎖定作業
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefd9b292747e89f5ebafd94cb8aa0e38833e8cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513420"
---
# <a name="opportunistic-lock-operations"></a><span data-ttu-id="43f21-103">隨機鎖定作業</span><span class="sxs-lookup"><span data-stu-id="43f21-103">Opportunistic Lock Operations</span></span>

<span data-ttu-id="43f21-104">如果應用程式要求隨機鎖定，則必須使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函式搭配檔案 **\_ 旗 \_** 標重迭旗標，開啟其要求鎖定的所有檔案，以便重迭 (非同步) 輸入和輸出。</span><span class="sxs-lookup"><span data-stu-id="43f21-104">If an application requests opportunistic locks, all files for which it requests locks must be opened for overlapped (asynchronous) input and output by using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function with the **FILE\_FLAG\_OVERLAPPED** flag.</span></span> <span data-ttu-id="43f21-105">開啟檔案以進行重迭的作業之後，您可以使用 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函式搭配下列其中一個控制程式代碼來處理這些檔案的隨機鎖定：</span><span class="sxs-lookup"><span data-stu-id="43f21-105">After the files are opened for overlapped operation, you can use the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with one of the following control codes to work with those files' opportunistic locks:</span></span>

<dl>

[<span data-ttu-id="43f21-106">**FSCTL \_ OPBATCH \_ ACK \_ 關閉 \_ 擱置中**</span><span class="sxs-lookup"><span data-stu-id="43f21-106">**FSCTL\_OPBATCH\_ACK\_CLOSE\_PENDING**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[<span data-ttu-id="43f21-107">**FSCTL \_ OPLOCK \_ 中斷 \_ ACK \_ 無 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="43f21-107">**FSCTL\_OPLOCK\_BREAK\_ACK\_NO\_2**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[<span data-ttu-id="43f21-108">**FSCTL \_ OPLOCK \_ BREAK \_ 確認**</span><span class="sxs-lookup"><span data-stu-id="43f21-108">**FSCTL\_OPLOCK\_BREAK\_ACKNOWLEDGE**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[<span data-ttu-id="43f21-109">**FSCTL \_ OPLOCK \_ 中斷 \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="43f21-109">**FSCTL\_OPLOCK\_BREAK\_NOTIFY**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[<span data-ttu-id="43f21-110">**FSCTL \_ 要求 \_ 批次 \_ OPLOCK**</span><span class="sxs-lookup"><span data-stu-id="43f21-110">**FSCTL\_REQUEST\_BATCH\_OPLOCK**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[<span data-ttu-id="43f21-111">**FSCTL \_ 要求 \_ 篩選 \_ OPLOCK**</span><span class="sxs-lookup"><span data-stu-id="43f21-111">**FSCTL\_REQUEST\_FILTER\_OPLOCK**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[<span data-ttu-id="43f21-112">**FSCTL \_ 要求 \_ OPLOCK**</span><span class="sxs-lookup"><span data-stu-id="43f21-112">**FSCTL\_REQUEST\_OPLOCK**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[<span data-ttu-id="43f21-113">**FSCTL \_ 要求 \_ OPLOCK \_ 層級 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="43f21-113">**FSCTL\_REQUEST\_OPLOCK\_LEVEL\_1**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[<span data-ttu-id="43f21-114">**FSCTL \_ 要求 \_ OPLOCK \_ 層級 \_ 2**</span><span class="sxs-lookup"><span data-stu-id="43f21-114">**FSCTL\_REQUEST\_OPLOCK\_LEVEL\_2**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

 

 
