---
title: 裝置存取詞彙
description: 以下是在裝置存取 API 的檔中使用的詞彙。
Robots: noindex, nofollow
ms.assetid: A6311538-D7CC-4A23-A145-14AF3BBFC4C4
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 8406c41a2666f9014bac27452572c6f88b84e6bf
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/11/2020
ms.locfileid: "104374342"
---
# <a name="device-access-glossary"></a>裝置存取詞彙

以下是在裝置存取 API 的檔中使用的詞彙。

<dl> <dt>

**AppContainer**
</dt> <dd>

高度受限的執行環境，在此環境中，進程會以精簡的使用者許可權子集來執行。 在 AppContainer 內執行的進程稱為 AppContainer 處理常式。 AppContainer 進程與其他 AppContainer 進程和使用者的設定檔隔離。 它對一小部分的系統資源（例如檔案、裝置、登錄機碼、處理序間通訊 (IPC) /remote 程序呼叫 (RPC) 端點和網路資源）具有有限的存取權。

</dd> <dt>

**繫結**
</dt> <dd>

將裝置存取物件與特定裝置介面產生關聯。 如果系結成功，Windows Store 應用程式就可以使用裝置存取物件作為訊息代理程式來與設備磁碟機進行通訊。

</dd> <dt>

**Broker**
</dt> <dd>

元件，可存取預設不會授與的資源。

</dd> <dt>

**具特殊許可權的應用程式**
</dt> <dd>

在特定裝置的中繼資料中識別為與該裝置相關聯的應用程式，讓它可以與設備磁碟機的受限制介面進行通訊。 這類應用程式的範例可能是專屬的音樂播放應用程式，當競爭者的應用程式無法使用時，其具有與便攜音樂播放機同步的獨佔許可權。 如需有關如何設定裝置的中繼資料，或如何將驅動程式限制在特殊許可權應用程式的詳細資訊，請參閱 [適用于內部裝置的 UWP 裝置應用程式](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices)。

</dd> </dl>
