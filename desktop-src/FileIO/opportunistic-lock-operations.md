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
# <a name="opportunistic-lock-operations"></a>隨機鎖定作業

如果應用程式要求隨機鎖定，則必須使用 [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) 函式搭配檔案 **\_ 旗 \_** 標重迭旗標，開啟其要求鎖定的所有檔案，以便重迭 (非同步) 輸入和輸出。 開啟檔案以進行重迭的作業之後，您可以使用 [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) 函式搭配下列其中一個控制程式代碼來處理這些檔案的隨機鎖定：

<dl>

[**FSCTL \_ OPBATCH \_ ACK \_ 關閉 \_ 擱置中**](/windows/win32/api/winioctl/ni-winioctl-fsctl_opbatch_ack_close_pending)  
[**FSCTL \_ OPLOCK \_ 中斷 \_ ACK \_ 無 \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_ack_no_2)  
[**FSCTL \_ OPLOCK \_ BREAK \_ 確認**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_acknowledge)  
[**FSCTL \_ OPLOCK \_ 中斷 \_ 通知**](/windows/win32/api/winioctl/ni-winioctl-fsctl_oplock_break_notify)  
[**FSCTL \_ 要求 \_ 批次 \_ OPLOCK**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_batch_oplock)  
[**FSCTL \_ 要求 \_ 篩選 \_ OPLOCK**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_filter_oplock)  
[**FSCTL \_ 要求 \_ OPLOCK**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock)  
[**FSCTL \_ 要求 \_ OPLOCK \_ 層級 \_ 1**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_1)  
[**FSCTL \_ 要求 \_ OPLOCK \_ 層級 \_ 2**](/windows/win32/api/winioctl/ni-winioctl-fsctl_request_oplock_level_2)  
</dl>

 

 
