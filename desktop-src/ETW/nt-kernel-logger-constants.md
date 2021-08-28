---
description: 使用下列常數來識別 NT Kernel 記錄器會話。
ms.assetid: f64f05c1-b904-4847-8502-4abb9cf4d37f
title: NT 核心記錄器常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5fb3459415cf4d7fd5db8c9407ad102b741a35
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481694"
---
# <a name="nt-kernel-logger-constants"></a>NT 核心記錄器常數

使用下列常數來識別 NT Kernel 記錄器會話。



| 常數               | 描述                                                      |
|------------------------|------------------------------------------------------------------|
| SystemTraceControlGuid | NT 核心記錄器事件追蹤會話的控制項 GUID。 |
| 核心 \_ 記錄器 \_ 名稱   | NT 核心記錄器事件追蹤會話的名稱。          |



 

NT Kernel 記錄器會話是唯一可接受來自核心事件提供者事件的會話。 NT 核心記錄器會話不接受來自其他提供者的事件。 如果您想要從其他提供者捕獲核心事件和事件，您必須使用兩個不同的會話，而且取用者需要合併記錄檔中的事件，以提供端對端結果。

ETW 使用定義 \_ guid 宏來定義 guid。 若要在您的程式碼中使用 **SystemTraceControlGuid** ，您必須 \# 先包含定義 INITGUID，然後再包含 Evntrace. h。 編譯器接著會將定義 \_ guid 轉換成常數 guid。

下列值會定義 NT Kernel 記錄器會話可以追蹤的核心事件可能的類別 Guid。 您可以將類別 Guid 傳遞至 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式，以設定每個事件類別的特殊處理。




| 類別 | GUID | 
|-------|------|
| <a href="alpc.md"><strong>ALPC</strong></a> | <pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 45d8cccd-539f-4b72-a8b7-5c683142609a */    ALPCGuid,    0x45d8cccd,    0x539f,    0x4b72,    0xa8, 0xb7, 0x5c, 0x68, 0x31, 0x42, 0x60, 0x9a  );</code></pre> | 
| <a href="diskio.md"><strong>DiskIo</strong></a> | <pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 3d6fa8d4-fe05-11d0-9dda-00c04fd7ba7c */    DiskIoGuid,    0x3d6fa8d4,    0xfe05,    0x11d0,    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c  );</code></pre> | 
| <a href="hwconfig.md"><strong>HWConfig</strong></a>和<a href="systemconfig.md"> <strong>SystemConfig</strong></a> | <pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 01853a65-418f-4f36-aefc-dc0f1d2fd235 */    EventTraceConfigGuid,    0x01853a65,    0x418f,    0x4f36,    0xae, 0xfc, 0xdc, 0x0f, 0x1d, 0x2f, 0xd2, 0x35  );</code></pre> | 
| <a href="fileio.md"><strong>FileIo</strong></a> | <pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 90cbdc39-4a3e-11d1-84f4-0000f80464e3 */    FileIoGuid,    0x90cbdc39,    0x4a3e,    0x11d1,    0x84, 0xf4, 0x00, 0x00, 0xf8, 0x04, 0x64, 0xe3  );</code></pre> | 
| <a href="image.md"><strong>圖像</strong></a> | <pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 2cb15d1d-5fc1-11d2-abe1-00a0c911f518 */    ImageLoadGuid,    0x2cb15d1d,    0x5fc1,    0x11d2,    0xab, 0xe1, 0x00, 0xa0, 0xc9, 0x11, 0xf5, 0x18  );</code></pre> | 
| <a href="pagefault-v2.md"><strong>PageFault_V2</strong></a> | <pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 3d6fa8d3-fe05-11d0-9dda-00c04fd7ba7c */    PageFaultGuid,    0x3d6fa8d3,    0xfe05,    0x11d0,    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c  );</code></pre> | 
| <a href="perfinfo.md"><strong>PerfInfo</strong></a> | <pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* ce1dbfb4-137e-4da6-87b0-3f59aa102cbc */    PerfInfoGuid,    0xce1dbfb4,    0x137e,    0x4da6,    0x87, 0xb0, 0x3f, 0x59, 0xaa, 0x10, 0x2c, 0xbc  );</code></pre> | 
| <a href="process.md"><strong>處理序</strong></a> | <pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 3d6fa8d0-fe05-11d0-9dda-00c04fd7ba7c */    ProcessGuid,    0x3d6fa8d0,    0xfe05,    0x11d0,    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c  );</code></pre> | 
| <a href="registry.md"><strong>登錄</strong></a> | <pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* AE53722E-C863-11d2-8659-00C04FA321A1 */    RegistryGuid,     0xae53722e,    0xc863,    0x11d2,    0x86, 0x59, 0x0, 0xc0, 0x4f, 0xa3, 0x21, 0xa1);</code></pre> | 
| <a href="splitio.md"><strong>SplitIo</strong></a> | <pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* d837ca92-12b9-44a5-ad6a-3a65b3578aa8 */    SplitIoGuid,     0xd837ca92,    0x12b9,    0x44a5,    0xad, 0x6a, 0x3a, 0x65, 0xb3, 0x57, 0x8a, 0xa8);</code></pre> | 
| <a href="tcpip.md"><strong>Tcpip.sys</strong></a> | <pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 9a280ac0-c8e0-11d1-84e2-00c04fb998a2 */    TcpIpGuid,    0x9a280ac0,    0xc8e0,    0x11d1,    0x84, 0xe2, 0x00, 0xc0, 0x4f, 0xb9, 0x98, 0xa2  );</code></pre> | 
| <a href="thread.md"><strong>執行緒</strong></a> | <pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* 3d6fa8d1-fe05-11d0-9dda-00c04fd7ba7c */    ThreadGuid,    0x3d6fa8d1,    0xfe05,    0x11d0,    0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c  );</code></pre> | 
| <a href="udpip.md"><strong>UdpIp</strong></a> | <pre class="syntax" data-space="preserve"><code>DEFINE_GUID ( /* bf3a50c5-a9c9-4988-a005-2df0b7c80f80 */    UdpIpGuid,    0xbf3a50c5,    0xa9c9,    0x4988,    0xa0, 0x05, 0x2d, 0xf0, 0xb7, 0xc8, 0x0f, 0x80  );</code></pre> | 




 

## <a name="remarks"></a>備註

若要使用 Guid，請將您要使用的 GUID 定義複製到您的原始程式碼。 您必須在 \# 原始程式碼中包含的定義之前包含定義 INITGUID，讓編譯器將定義 \_ guid 轉換成常數 guid。 例如

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

或者，您也可以自行定義 GUID 定義的常數 GUID。 例如

``` syntax
static const GUID ThreadGuid = 
{ 0x3d6fa8d0, 0xfe05, 0x11d0, { 0x9d, 0xda, 0x00, 0xc0, 0x4f, 0xd7, 0xba, 0x7c } };
```

 

 
