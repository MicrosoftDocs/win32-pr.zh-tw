---
description: 支援 MTP 擴充功能
ms.assetid: 9e5f3da6-346a-4eca-bc85-2755c569986d
title: 支援 MTP 擴充功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16a80b640b50346f1724aec771d8ffd82de565f078e5b3e1d562c346e34973a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193569"
---
# <a name="supporting-mtp-extensions"></a>支援 MTP 擴充功能

## <a name="media-transfer-protocol"></a>媒體傳輸通訊協定

媒體傳輸通訊協定 (MTP) 是圖片傳輸通訊協定 (PTP) 的延伸模組。 因此，所有的 PTP 通訊協定語法在 MTP 中都有效。

MTP 會使用兩方、起始端和回應者之間的命令和回應進行通訊。 相關裝置的角色很清楚地定義。 電腦通常是起始端，而裝置一律是回應者。 非電腦裝置也可以是啟動者 (例如，汽車組或 Microsoft X box) 。 裝置絕對不能同時採用這兩個角色。

啟動器會將命令傳送至回應程式以開始通訊。 回應程式會處理此命令並傳回適當的回應。 可能會有與命令相關聯的資料階段。 如果是這種情況，則必須事先知道資料流程的方向，並由起始端和回應者接受。 請注意，沒有指出新命令之資料流程的描述性標頭。

回應程式可以啟動與啟動器無關的通訊。 例如，回應程式可以將事件傳送給啟動器。 但是，不能與事件一起傳送任何資料。 如果有任何需要在事件中讀取的資料，啟動者必須傳送 MTP 命令，然後裝置可以傳送資料以回應命令。

如需 MTP 的完整說明，請參閱 [mtp 規格](https://www.usb.org/sites/default/files/MTPv1_1.zip)。

## <a name="sending-mtp-commands"></a>傳送 MTP 命令

應用程式可以藉由叫用 [**IPortableDevice：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) 方法，將 MTP 命令傳送至裝置。 傳送的命令取決於是否有資料階段，以及是否有任何伴隨的資料讀取或寫入至裝置。 下表描述三個可能的 MTP 延伸模組命令。

請注意，這些命令是 MTP 專用的。因此，只由 WPD MTP 類別驅動程式所執行。



| 命令  | 描述  |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**WPD \_ 命令 \_ MTP \_ EXT \_ END \_ DATA \_ TRANSFER**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-end-data-transfer)                                      | 發出 MTP 命令，以對資料讀取或寫入作業的結束髮出信號。              |
| [**WPD \_ 命令 \_ MTP \_ EXT \_ EXECUTE \_ 命令（ \_ 不含 \_ 資料 \_ 階段）**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-without-data-phase)  | 發出 MTP 命令，而不使用對應的資料階段。                                         |
| [**WPD \_ 命令 \_ MTP \_ EXT \_ EXECUTE \_ 命令 \_ 與 \_ \_ 要 \_ 寫入的資料**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) | 發出 MTP 命令，其後伴隨的資料會寫入至裝置。 |
| [**WPD \_ 命令 \_ MTP \_ EXT \_ EXECUTE \_ 命令 \_ 與 \_ \_ 要 \_ 讀取的資料**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read)   | 發出 MTP 命令，後面接著伴隨的資料（從裝置讀取）。       |
| [**WPD \_ 命令 \_ MTP \_ EXT \_ 讀取 \_ 資料**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-read-data)                                                       | 發出 MTP 命令，此命令會將資料從裝置傳送到電腦。                                  |
| [**WPD \_ 命令 \_ MTP \_ EXT \_ 寫入 \_ 資料**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-write-data)                                                     | 發出 MTP 命令，此命令會從電腦將資料傳送至裝置。                                  |



 

無論該階段為何，都必須指定 **WPD \_ 屬性 \_ mtp \_ ext \_ \_** ext operation 程式碼和 **WPD \_ 屬性 \_ mtp \_ ext ext 作業 \_ \_ 參數** 。

如果 MTP 驅動程式能夠將命令傳送至裝置，則傳回值一律會包含 **WPD \_ 屬性 \_ MTP \_ EXT 的 \_ 回應 \_ 碼**。 如果回應碼指出成功，而且命令的語法允許回應參數，則也會提供 **WPD \_ 屬性 \_ MTP \_ EXT \_ 回應 \_** 參數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 
