---
description: MFTrace 是一種工具，可為媒體基礎應用程式產生追蹤記錄。
ms.assetid: 55b421c8-e87c-4dd2-8649-93832c93f999
title: MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 542ac9325b33fc8f1a76394d203dbf1d27919bd6
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885222"
---
# <a name="mftrace"></a>MFTrace

MFTrace 是一種工具，可為媒體基礎應用程式產生追蹤記錄。

## <a name="in-this-section"></a>本節內容

-   [使用 MFTrace](using-mftrace.md)
-   [MFTrace 關鍵字](mftrace-keywords.md)
-   [MFTrace 設定檔](mftrace-configuration-file.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------------|---------------------------------------------------------------------------------------|
| 最低 SDK 版本      | 適用于 Windows 7 和 .NET Framework 4.0 的 Microsoft Windows 軟體開發套件 (SDK)  |
| 最低作業系統 | Windows Vista                                                                         |



 

MFTrace 需要下列 Dll，這些 Dll 也會在 SDK 中提供。

-   detoured.dll
-   mfdetours.dll

SDK 提供32位和64位版本的 MFTrace。 MFTrace 不支援 WOW64;若要追蹤在64位 Windows 上執行的32位進程，請使用32位版本的 MFTrace。

sdk-32 位系統上的根目錄： \Program files \ Windows Kits\10 sdk-64 位系統上的根目錄： \Program Files (x86) \ Windows Kits\10 您將在 &lt; sdk-根 &gt; \bin \<sdk-version> \<architecture>\mftrace.exe 找到 mftrace

## <a name="related-topics"></a>相關主題

<dl> <dt>

[媒體基礎工具](media-foundation-tools.md)
</dt> </dl>

 

 



