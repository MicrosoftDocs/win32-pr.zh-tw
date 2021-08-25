---
title: Server-Side 設定消費者介面
description: 藉由執行 COM 介面 IEAPProviderConfig，來為伺服器執行設定 UI。
ms.assetid: b205c573-6694-42c0-b4f1-1480932dd644
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92bf6a1f5b5f0e1302e68dd8ca9070771bfbc7714759a384f67782ffdad6e2ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021808"
---
# <a name="server-side-configuration-user-interface"></a>Server-Side 設定消費者介面

藉由執行 COM 介面 [**IEAPProviderConfig**](/previous-versions/windows/desktop/api/Rrascfg/nn-rrascfg-ieapproviderconfig)，來為伺服器執行設定 UI。 這個 COM 介面衍生自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 並加入三個方法： [**IEAPProviderConfig：： Initialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-initialize)、 [**IEAPProviderConfig：： ServerInvokeConfigUI**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-serverinvokeconfigui)和 [**IEAPProviderConfig：：**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-uninitialize)Initialize。

UI 應該支援遠端系統管理。 換句話說，雖然 UI 會設定伺服器上的驗證通訊協定，但是 UI 本身也可能在不同的電腦上執行。 若要支援遠端系統管理，請將 UI 程式碼與實際執行設定的程式碼分開。 設定程式碼位於驗證通訊協定執行所在的伺服器上。

使用 Active Template Library (ATL) 來執行 [**IEAPProviderConfig**](/previous-versions/windows/desktop/api/Rrascfg/nn-rrascfg-ieapproviderconfig)。 如需詳細資訊，請參閱 SDK 範例目錄中的伺服器端設定 UI 範例。 設定 UI 物件 (CLSID) 的類別識別碼應放置在登錄中，並將值名稱設為 [RAS \_ EAP \_ VALUENAME \_ CONFIG \_ CLSID](authentication-protocol-registry-values.md)。 如需詳細資訊，請參閱 [驗證通訊協定登錄值](authentication-protocol-registry-values.md)。

當使用者在 [路由] 和 [RAS] 的 [內容] 對話方塊中按一下驗證通訊協定的 [設定] 按鈕時，系統會檢查 \_ \_ \_ \_ 登錄中是否有此驗證通訊協定的 RAS EAP VALUENAME 設定 CLSID 值。 如果是，COM 會將設定 UI 物件具現化。 如果系統在登錄中找不到 RAS \_ EAP \_ VALUENAME 設定 \_ \_ CLSID，而且系統可存取 (DS) 的目錄服務，系統會嘗試從類別存放區具現化物件。

如果使用者同時連線到多部電腦，則會具現化多個設定 UI 物件。

 

 