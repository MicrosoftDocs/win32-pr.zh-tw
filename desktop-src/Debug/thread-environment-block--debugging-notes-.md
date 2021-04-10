---
description: '執行緒環境區塊 (調試附注) '
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: '執行緒環境區塊 (調試附注) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d66b04b522bed8bdf7f5a5571c300019e4537b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847303"
---
# <a name="thread-environment-block-debugging-notes"></a>執行緒環境區塊 (調試附注) 

執行緒環境區塊 ([**TEB 結構**](/windows/win32/api/winternl/ns-winternl-teb)) 保存執行緒的內容資訊。

在下列版本的 Windows 中，64位 TEB 內32位 TEB 位址的位移是0。 這可以用來直接存取 WOW64 執行緒的32位 TEB。 在較新版本的 Windows 中，這可能會變更



|               |                        |
|---------------|------------------------|
| Windows Vista | Windows Server 2008    |
| Windows 7     | Windows Server 2008 R2 |
| Windows 8     | Windows Server 2012    |
| Windows 8.1   | Windows Server 2012 R2 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[偵錯結構](debugging-structures.md)
</dt> <dt>

[**WOW64 \_ 內容**](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
