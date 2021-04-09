---
title: WsUtil 編譯器工具
description: WsUtil.exe 的 Windows Web 服務編譯器工具支援服務模型和資料類型的序列化。 它會處理 WSDL、XML 架構和原則檔，並產生 C 標頭和原始程式檔。
ms.assetid: 7fc3f1bd-ead2-4095-9592-d2ad88d56e7a
keywords:
- 適用于 Windows 的 WsUtil 編譯器工具 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa83da50888fcf2d66fac7fb00b3a31ae2919738
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933733"
---
# <a name="wsutil-compiler-tool"></a>WsUtil 編譯器工具

WsUtil.exe 的 Windows Web 服務編譯器工具支援 [服務模型](service-model-layer-overview.md) 和資料類型的 [序列化](serialization.md) 。 它會處理 WSDL、XML 架構和原則檔，並產生 C 標頭和原始程式檔。 這項工具與適用于 managed 程式碼的 WSDL 編譯器工具類似，但其目的是改為原生程式碼。

為了支援 [服務模型](service-model-layer-overview.md)，WsUtil.exe 會產生用於用戶端和服務的標頭。 它會視需要產生用戶端的 C proxy 檔案，以及服務端的 C 存根檔案。

為了支援 [序列化](serialization.md)，編譯器會針對全域專案定義產生專案描述的標頭，以及序列化引擎所取用之 proxy 檔案中的所有類型定義資訊。


如需處理 WSDL 檔案、XML 架構檔案和 web 服務原則檔案的命令列選項，請參閱下列主題：

-   [Web 服務編譯器工具](web-service-compiler-tool.md)
-   [WSDL 和服務合約](wsdl-support.md)
-   [結構描述支援](schema-support.md)
-   [原則支援](policy-support.md)

## <a name="security"></a>安全性

當您使用 WsUtil 時，請注意下列問題，並觀察適當的預防措施：

-   Wsutil 不會透過網路抓取 XML 中繼資料，而且 Wsutil 無法解析輸入中繼資料檔案中的 import 和/或 include 語句。 Wsutil 會開啟並讀取 wsdl、xsd 和原則檔。 XML 中繼資料不會受到防篡改。 請確定您只使用 wsdl、xsd 和原則檔案是從受信任的來源取得，並且確定在使用檔案之前和之後都不會受到篡改的保護。 仔細檢查輸入檔的內容，並驗證檔案的內容可安全地在應用程式中使用。 Wsutil.exe 不會針對中繼資料檔案的真實性進行任何驗證。
-   Wsutil 會產生標頭和存根檔案，這些檔案不會受到防篡改。 您必須在 wsutil.exe 所產生的原始程式檔上設定正確的層級存取權限，以防止 unauthoritized 存取這些檔案。 Wsutil 會使用 StreamWriter 來建立輸出檔。
-   使用者必須留意到 Wsutil 可以覆寫本機檔案，而且使用/out 參數指定輸出檔的安全檔案名和目錄時，也應該小心。
-   在 wsutil.exe 中載入的 Wsutil 或 wsutilhelper.dll，可能會在攻擊或處理非常大量的輸入中繼資料時，非預期地終止或耗用大量的系統資源。 此工具是設計用來在開發期間使用，只應使用此工具作為開發時間工具。 在仲介層中使用可能無法安全地處理原則資訊。
-   Wsutilhelper.dll helper DLL 會載入至 managed wsutil.exe 來處理原則資訊。 使用者應確定二進位路徑中不存在具有相同檔案名的惡意二進位檔。 同樣地，使用者應確定在組建環境中，已正確設定二進位路徑，且不存在具有相同 "wsutil.exe" 名稱的惡意二進位檔。
-   如果可能的話，Wsutil 會為作業和結構欄位產生 SAL 注釋。 Wsutil 產生之檔案的使用者應遵循透過 SAL 注釋指定的需求。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[服務模型層總覽](service-model-layer-overview.md)
</dt> <dt>

[序列 化](serialization.md)
</dt> <dt>

[Web 服務編譯器工具](web-service-compiler-tool.md)
</dt> <dt>

[WSDL 支援](wsdl-support.md)
</dt> <dt>

[結構描述支援](schema-support.md)
</dt> <dt>

[原則支援](policy-support.md)
</dt> </dl>

 

 




