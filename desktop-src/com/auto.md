---
title: 自動
description: 判斷在傳送 COM RPC 通知時是否自動啟動偵錯工具。
ms.assetid: e05ae7cb-79d1-4543-aef3-9397548c2030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23c7730c3c6e0fe9dc01b43a7c4f9621897f9f16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966217"
---
# <a name="auto"></a><span data-ttu-id="51a80-103">自動</span><span class="sxs-lookup"><span data-stu-id="51a80-103">Auto</span></span>

<span data-ttu-id="51a80-104">判斷在傳送 COM RPC 通知時是否自動啟動偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="51a80-104">Determines if the debugger is automatically launched when a COM RPC notification is sent.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="51a80-105">登錄項目</span><span class="sxs-lookup"><span data-stu-id="51a80-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\DebugObjectRPCEnabled\AeDebug
   Auto = value
```

## <a name="remarks"></a><span data-ttu-id="51a80-106">備註</span><span class="sxs-lookup"><span data-stu-id="51a80-106">Remarks</span></span>

<span data-ttu-id="51a80-107">這是 **REG \_ 單字** 值。</span><span class="sxs-lookup"><span data-stu-id="51a80-107">This is a **REG\_WORD** value.</span></span>



| <span data-ttu-id="51a80-108">值</span><span class="sxs-lookup"><span data-stu-id="51a80-108">Value</span></span> | <span data-ttu-id="51a80-109">描述</span><span class="sxs-lookup"><span data-stu-id="51a80-109">Description</span></span>                    |
|-------|--------------------------------|
| <span data-ttu-id="51a80-110">1</span><span class="sxs-lookup"><span data-stu-id="51a80-110">1</span></span>     | <span data-ttu-id="51a80-111">自動啟動偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="51a80-111">Automatically launch debugger.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="51a80-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="51a80-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="51a80-113">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="51a80-113">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="51a80-114">**IOrpcDebugNotify**</span><span class="sxs-lookup"><span data-stu-id="51a80-114">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> <dt>

[<span data-ttu-id="51a80-115">**ORPC \_ DBG \_ ALL**</span><span class="sxs-lookup"><span data-stu-id="51a80-115">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> </dl>

 

 




