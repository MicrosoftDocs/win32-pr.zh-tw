---
description: 網路 DDE 使用受信任的共用和安全描述項來控制對共用的存取。
ms.assetid: a22d9fc6-a0c9-442f-b278-1271cfbc636b
title: 受信任的共用和安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22bed3b520597f6cabe95929d2ee5bf9c29af6bb6c524d2aa136f4c86392cbb8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014678"
---
# <a name="trusted-shares-and-security"></a>受信任的共用和安全性

\[不再支援網路 DDE。 Nddeapi.dll 存在於 Windows Vista 中，但所有的函式呼叫會傳回 NDDE \_ 未 \_ 執行。\]

網路 DDE 使用受信任的共用和安全描述項來控制對共用的存取。

## <a name="trusted-shares"></a>信任的共用

當用戶端使用者從遠端電腦連接到 DDE 共用時，只有在下列陳述成立時，網路 DDE 才會接受要求：

-   建立共用的使用者已透過呼叫 [**NDdeSetTrustedShare**](nddesettrustedshare.md)，將信任的狀態授與共享。 只有共用的建立者可以將信任狀態授與共享。 系統管理員甚至不能將受信任的狀態授與給不同使用者所建立的 DDE 共用。
-   建立共用的使用者目前已登入伺服器電腦。

將信任狀態授與共享的程式，會將共用新增至 DSDM 中已登入使用者的受信任共用清單。 這會在伺服器及其用戶端之間建立信任關係。 當 DDE 共用有受信任狀態時，只要建立共用的使用者登入，用戶端就可以連線到該狀態。 當用戶端從遠端電腦連接到共用時，只有在 DSDM 中已登入使用者的受信任共用清單中列出共用時，網路 DDE 才會接受要求。

## <a name="security"></a>安全性

當用戶端要求資料或連結時，網路 DDE 會執行額外的安全性檢查。 它會檢查伺服器是否已為遠端使用者授與操作的必要許可權。 伺服器會透過 [**NDdeShareAdd**](nddeshareadd.md)函數的 *pSD* 參數，控制對共用的存取。 此參數會指定安全描述項。 如果此參數為 **Null**，此函式會建立預設安全描述項，以授與共享建立者的完整存取權，並將讀取和連結許可權授與所有其他使用者。 若要授與或拒絕個別使用者或使用者群組的其他許可權，請建立並使用安全描述項。 如需安全描述項的詳細資訊，請參閱 [**存取控制**](/windows/desktop/SecAuthZ/access-control)。

若要取得現有 DDE 共用的安全描述項，請呼叫 [**NDdeGetShareSecurity**](nddegetsharesecurity.md) 函數。 您可以編輯資訊，然後使用 [**NDdeSetShareSecurity**](nddesetsharesecurity.md) 函數來更新共用的安全描述項。

 

 
