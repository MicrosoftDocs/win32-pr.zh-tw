---
description: 使用下列常數來識別 NT Kernel 記錄器會話。
ms.assetid: f64f05c1-b904-4847-8502-4abb9cf4d37f
title: NT 核心記錄器常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13767400ff851e358f6665c88e16767cc378a4da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973717"
---
# <a name="nt-kernel-logger-constants"></a><span data-ttu-id="93537-103">NT 核心記錄器常數</span><span class="sxs-lookup"><span data-stu-id="93537-103">NT Kernel Logger Constants</span></span>

<span data-ttu-id="93537-104">使用下列常數來識別 NT Kernel 記錄器會話。</span><span class="sxs-lookup"><span data-stu-id="93537-104">Use the following constants to identify the NT Kernel Logger session.</span></span>



| <span data-ttu-id="93537-105">常數</span><span class="sxs-lookup"><span data-stu-id="93537-105">Constant</span></span>               | <span data-ttu-id="93537-106">描述</span><span class="sxs-lookup"><span data-stu-id="93537-106">Description</span></span>                                                      |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="93537-107">SystemTraceControlGuid</span><span class="sxs-lookup"><span data-stu-id="93537-107">SystemTraceControlGuid</span></span> | <span data-ttu-id="93537-108">NT 核心記錄器事件追蹤會話的控制項 GUID。</span><span class="sxs-lookup"><span data-stu-id="93537-108">The control GUID for the NT Kernel Logger event tracing session.</span></span> |
| <span data-ttu-id="93537-109">核心 \_ 記錄器 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="93537-109">KERNEL\_LOGGER\_NAME</span></span>   | <span data-ttu-id="93537-110">NT 核心記錄器事件追蹤會話的名稱。</span><span class="sxs-lookup"><span data-stu-id="93537-110">The name of the NT Kernel Logger event tracing session.</span></span>          |



 

<span data-ttu-id="93537-111">NT Kernel 記錄器會話是唯一可接受來自核心事件提供者事件的會話。</span><span class="sxs-lookup"><span data-stu-id="93537-111">The NT Kernel Logger session is the only session that can accept events from kernel event providers.</span></span> <span data-ttu-id="93537-112">NT 核心記錄器會話不接受來自其他提供者的事件。</span><span class="sxs-lookup"><span data-stu-id="93537-112">The NT Kernel Logger session does not accept events from other providers.</span></span> <span data-ttu-id="93537-113">如果您想要從其他提供者捕獲核心事件和事件，您必須使用兩個不同的會話，而且取用者需要合併記錄檔中的事件，以提供端對端結果。</span><span class="sxs-lookup"><span data-stu-id="93537-113">If you want to capture kernel events and events from other providers, you must use two separate sessions and the consumer would need to merge the events from the log files to provide end-to-end results.</span></span>

<span data-ttu-id="93537-114">ETW 使用定義 \_ guid 宏來定義 guid。</span><span class="sxs-lookup"><span data-stu-id="93537-114">ETW uses the DEFINE\_GUID macro to define GUIDs.</span></span> <span data-ttu-id="93537-115">若要在您的程式碼中使用 **SystemTraceControlGuid** ，您必須 \# 先包含定義 INITGUID，然後再包含 Evntrace. h。</span><span class="sxs-lookup"><span data-stu-id="93537-115">To use **SystemTraceControlGuid** in your code, you must include \#define INITGUID before including Evntrace.h.</span></span> <span data-ttu-id="93537-116">編譯器接著會將定義 \_ guid 轉換成常數 guid。</span><span class="sxs-lookup"><span data-stu-id="93537-116">The compiler will then turn the DEFINE\_GUID into a constant GUID.</span></span>

<span data-ttu-id="93537-117">下列值會定義 NT Kernel 記錄器會話可以追蹤的核心事件可能的類別 Guid。</span><span class="sxs-lookup"><span data-stu-id="93537-117">The following values define the possible class GUIDs for kernel events that an NT Kernel Logger session can trace.</span></span> <span data-ttu-id="93537-118">您可以將類別 Guid 傳遞至 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式，以設定每個事件類別的特殊處理。</span><span class="sxs-lookup"><span data-stu-id="93537-118">You can pass the class GUIDs to the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function to set up special processing for each event class.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93537-119">類別</span><span class="sxs-lookup"><span data-stu-id="93537-119">Class</span></span></th>
<th><span data-ttu-id="93537-120">GUID</span><span class="sxs-lookup"><span data-stu-id="93537-120">GUID</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93537-121"><a href="alpc.md"><strong>ALPC</strong></a></span><span class="sxs-lookup"><span data-stu-id="93537-121"><a href="alpc.md"><strong>ALPC</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 45d8cccd-539f-4b72-a8b7-5c683142609a */
    ALPCGuid,
    0x45d8cccd,
    0x539f,
    0x4b72,
    0xa8, 0xb7, 0x5c, 0x68, 0x31, 0x42, 0x60, 0x9a
  );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93537-122"><a href="diskio.md"><strong>DiskIo</strong></a></span><span class="sxs-lookup"><span data-stu-id="93537-122"><a href="diskio.md"><strong>DiskIo</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 3d6fa8d4-fe05-11d0-9dda-00c04fd7ba7c */
    DiskIoGuid,
    0x3d6fa8d4,
    0xfe05,
    0x11d0,
    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c
  );</code></pre></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93537-123"><a href="hwconfig.md"><strong>HWConfig</strong></a>和<a href="systemconfig.md"> <strong>SystemConfig</strong></a></span><span class="sxs-lookup"><span data-stu-id="93537-123"><a href="hwconfig.md"><strong>HWConfig</strong></a> and <a href="systemconfig.md"><strong>SystemConfig</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 01853a65-418f-4f36-aefc-dc0f1d2fd235 */
    EventTraceConfigGuid,
    0x01853a65,
    0x418f,
    0x4f36,
    0xae, 0xfc, 0xdc, 0x0f, 0x1d, 0x2f, 0xd2, 0x35
  );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93537-124"><a href="fileio.md"><strong>FileIo</strong></a></span><span class="sxs-lookup"><span data-stu-id="93537-124"><a href="fileio.md"><strong>FileIo</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 90cbdc39-4a3e-11d1-84f4-0000f80464e3 */
    FileIoGuid,
    0x90cbdc39,
    0x4a3e,
    0x11d1,
    0x84, 0xf4, 0x00, 0x00, 0xf8, 0x04, 0x64, 0xe3
  );</code></pre></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93537-125"><a href="image.md"><strong>Image</strong></a></span><span class="sxs-lookup"><span data-stu-id="93537-125"><a href="image.md"><strong>Image</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 2cb15d1d-5fc1-11d2-abe1-00a0c911f518 */
    ImageLoadGuid,
    0x2cb15d1d,
    0x5fc1,
    0x11d2,
    0xab, 0xe1, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x18
  );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93537-126"><a href="pagefault-v2.md"><strong>PageFault_V2</strong></a></span><span class="sxs-lookup"><span data-stu-id="93537-126"><a href="pagefault-v2.md"><strong>PageFault_V2</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 3d6fa8d3-fe05-11d0-9dda-00c04fd7ba7c */
    PageFaultGuid,
    0x3d6fa8d3,
    0xfe05,
    0x11d0,
    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c
  );</code></pre></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93537-127"><a href="perfinfo.md"><strong>PerfInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="93537-127"><a href="perfinfo.md"><strong>PerfInfo</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* ce1dbfb4-137e-4da6-87b0-3f59aa102cbc */
    PerfInfoGuid,
    0xce1dbfb4,
    0x137e,
    0x4da6,
    0x87, 0xb0, 0x3f, 0x59, 0xaa, 0x10, 0x2c, 0xbc
  );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93537-128"><a href="process.md"><strong>處理序</strong></a></span><span class="sxs-lookup"><span data-stu-id="93537-128"><a href="process.md"><strong>Process</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c */
    ProcessGuid,
    0x3d6fa8d0,
    0xfe05,
    0x11d0,
    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c
  );</code></pre></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93537-129"><a href="registry.md"><strong>登錄</strong></a></span><span class="sxs-lookup"><span data-stu-id="93537-129"><a href="registry.md"><strong>Registry</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* AE53722E-C863-11d2-8659-00C04FA321A1 */
    RegistryGuid, 
    0xae53722e,
    0xc863,
    0x11d2,
    0x86, 0x59, 0x0, 0xc0, 0x4f, 0xa3, 0x21, 0xa1
);</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93537-130"><a href="splitio.md"><strong>SplitIo</strong></a></span><span class="sxs-lookup"><span data-stu-id="93537-130"><a href="splitio.md"><strong>SplitIo</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* d837ca92-12b9-44a5-ad6a-3a65b3578aa8 */
    SplitIoGuid, 
    0xd837ca92,
    0x12b9,
    0x44a5,
    0xad, 0x6a, 0x3a, 0x65, 0xb3, 0x57, 0x8a, 0xa8
);</code></pre></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93537-131"><a href="tcpip.md"><strong>Tcpip.sys</strong></a></span><span class="sxs-lookup"><span data-stu-id="93537-131"><a href="tcpip.md"><strong>TcpIp</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 9a280ac0-c8e0-11d1-84e2-00c04fb998a2 */
    TcpIpGuid,
    0x9a280ac0,
    0xc8e0,
    0x11d1,
    0x84, 0xe2, 0x00, 0xc0, 0x4f, 0xb9, 0x98, 0xa2
  );</code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93537-132"><a href="thread.md"><strong>執行緒</strong></a></span><span class="sxs-lookup"><span data-stu-id="93537-132"><a href="thread.md"><strong>Thread</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c */
    ThreadGuid,
    0x3d6fa8d1,
    0xfe05,
    0x11d0,
    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c
  );</code></pre></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93537-133"><a href="udpip.md"><strong>UdpIp</strong></a></span><span class="sxs-lookup"><span data-stu-id="93537-133"><a href="udpip.md"><strong>UdpIp</strong></a></span></span></td>
<td><pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* bf3a50c5-a9c9-4988-a005-2df0b7c80f80 */
    UdpIpGuid,
    0xbf3a50c5,
    0xa9c9,
    0x4988,
    0xa0, 0x05, 0x2d, 0xf0, 0xb7, 0xc8, 0x0f, 0x80
  );</code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="93537-134">備註</span><span class="sxs-lookup"><span data-stu-id="93537-134">Remarks</span></span>

<span data-ttu-id="93537-135">若要使用 Guid，請將您要使用的 GUID 定義複製到您的原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="93537-135">To use the GUIDs, copy the GUID definitions that you want to use to your source code.</span></span> <span data-ttu-id="93537-136">您必須在 \# 原始程式碼中包含的定義之前包含定義 INITGUID，讓編譯器將定義 \_ guid 轉換成常數 guid。</span><span class="sxs-lookup"><span data-stu-id="93537-136">You must include \#define INITGUID before the definitions you include in your source code, so the compiler will turn the DEFINE\_GUID into a constant GUID.</span></span> <span data-ttu-id="93537-137">例如，</span><span class="sxs-lookup"><span data-stu-id="93537-137">For example,</span></span>

``` syntax
#define INITGUID

DEFINE_GUID ( /* 3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c */
    ThreadGuid,
    0x3d6fa8d1,
    0xfe05,
    0x11d0,
    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c
  );

DEFINE_GUID ( /* 3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c */
    ProcessGuid,
    0x3d6fa8d0,
    0xfe05,
    0x11d0,
    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c
  );
```

<span data-ttu-id="93537-138">或者，您也可以自行定義 GUID 定義的常數 GUID。</span><span class="sxs-lookup"><span data-stu-id="93537-138">As an alternative, you can define the constant GUID for the GUID definitions yourself.</span></span> <span data-ttu-id="93537-139">例如，</span><span class="sxs-lookup"><span data-stu-id="93537-139">For example,</span></span>

``` syntax
static const GUID ThreadGuid = 
{ 0x3d6fa8d0, 0xfe05, 0x11d0, { 0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c } };
```

 

 
