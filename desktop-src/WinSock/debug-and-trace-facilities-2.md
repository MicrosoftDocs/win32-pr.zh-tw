---
description: Debug 和 trace 設備和 Windows 通訊端2。
ms.assetid: eb29fc21-92d6-4471-860a-fd1c531686f6
title: Debug 和 Trace 設備
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae0617aa8fc18e90b0c3e366a7ab14f1457cb26471865bfcc97682801a858565
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741365"
---
# <a name="debug-and-trace-facilities"></a>Debug 和 Trace 設備

Windows通訊端2應用程式開發人員需要隔離錯誤：

-   應用程式。
-   *Ws2 \_32.dll* 或其中一個相容性填充碼 dll。
-   服務提供者。

Windows通訊端2透過數個元件和功能來解決這項需求：

-   Windows Vista 和更新版本上對 Winsock 追蹤的整合支援。
-   Windows Vista 上的 *Ws2 \_32.dll* 特別設計的 debug 版本。
-   用於 Windows Server 2003 和 Windows XP 上的個別基本偵錯工具和追蹤工具。

## <a name="winsock-tracing-using-event-tracing-for-windows"></a>使用事件追蹤進行 Windows 的 Winsock 追蹤

Windows Vista 和更新版本包含使用 Windows (ETW) 事件追蹤的 Winsock 追蹤的整合支援。 這是在 Windows Vista 和更新版本上追蹤 Winsock 呼叫的慣用方法。 使用 ETW 的 Winsock 追蹤很輕量，且適用于 Windows 的零售版本。 不需要額外的軟體或元件。 這項功能只需要在 Windows Vista 和更新版本上啟用。 如需詳細資訊，請參閱 [Winsock 追蹤](winsock-tracing.md) 主題。

## <a name="using-a-debug-version-of-ws2_32dll"></a>使用 Ws232.dll 的偵錯工具版本 \_

在 Windows Vista 和 Winsock 追蹤上， *Ws2 \_32.dll* 的偵錯工具組合，可讓您在 Windows 通訊端 2 API 或 SPI 之間進行所有程序呼叫，以進行監視和控制。

如果將 Windows Vista 的 Microsoft Windows 軟體開發套件 (SDK) 版本安裝到預設位置，則各種架構的 *Ws2 \_32.dll* 的 debug 版本都位於下列資料夾：

**C： \\ Program Files \\ Microsoft sdk \\ Windows \\ v 6.0 \\ NoRedist**

*Ws2 \_32.dll* 的已檢查版本符合 Windows 的版本，以及您要測試的 Service Pack。 請注意，可能已套用安全性修補程式，以更新您測試系統上的 *Ws2 \_32.dll* 。 Windows Vista 和舊版平臺軟體發展工具組的 Windows SDK (SDK) DVD/CD 訂用帳戶包含各種版本 Windows 的已檢查組建。 您應使用相同的 *Ws2 \_32.dll* 檢查版本，做為要測試之系統上所使用的零售版本。 另外也請注意，在已檢查的組建下執行的行為，不會與使用零售組建執行的行為相同。

**注意** Windows Server 2008 和更新版本的 Windows SDK 不再包含 *Ws2 \_32.dll* 的特殊偵錯工具版本。 開發人員應該改用使用 ETW 的 Winsock 追蹤，因為這項功能不需要 debug 組建。

## <a name="winsock-debug-and-trace-facility-on-windows-server-2003-and-windows-xp"></a>Windows Server 2003 和 Windows XP 上的 Winsock 調試和追蹤功能

在 Windows 8 之前的舊版 Windows，Windows Server 2012 支援個別的基本偵錯工具和追蹤功能，其中包含作為 Windows SDK 和舊版平臺 SDK 的範例。 只有在不支援 Winsock 追蹤的 Windows Server 2003 和 Windows XP 上，才應該使用 debug/trace 設備。

如果 Windows 7 的 Windows SDK 安裝到預設位置，則會在下列資料夾中安裝這個基本的 Winsock 追蹤功能：

**C： \\ Program Files \\ Microsoft sdk \\ Windows \\ 7.0 \\ 範例 \\ NetDs \\ winsock \\ dt \_ dll**

此資料夾中的 *DbgSpec.doc* 檔案提供此基本追蹤設備的相關檔。 您必須編譯 dt dll 資料夾中的範例程式碼 \_ ，才能使用此功能。 開發人員可自由使用原始程式碼開發符合其特定需求的 debug/trace DLL 版本。

請注意，這個基本的 Winsock 追蹤功能只適用于已安裝之 *Ws2 \_32.dll* 的偵錯工具版本。 因此您必須取得 *Ws2 \_32.dll* 的已檢查版本，使其符合您要測試的 Windows 版本和 Service Pack。

此基本 dt \_ dll 追蹤工具的限制在於，範例程式碼會針對每個 Winsock 函式呼叫使用全域鎖定 (重要區段) 。 這樣一來，這項功能就不太適合用來處理競爭情形。 您必須大幅重新撰寫範例程式碼，以使此追蹤設備適用于處理最真正的 Winsock 問題， (取代全域鎖定) 。 此範例程式碼可讓開發人員追蹤程序呼叫、程式傳回、參數值和傳回值。

開發人員可以使用這個基本機制來追蹤程序呼叫、程式傳回、參數值和傳回值。 在程序呼叫或程式傳回時，可以改變參數值和傳回值。 如有需要，可以防止或重新導向程序呼叫。 藉由存取此層級的資訊和控制，開發人員可以更妥善地找出應用程式、 *Ws2 \_32.dll* 或服務提供者的問題。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Winsock 追蹤](winsock-tracing.md)
</dt> </dl>

 

 



