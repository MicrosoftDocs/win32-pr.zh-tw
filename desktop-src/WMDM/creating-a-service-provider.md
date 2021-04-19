---
title: 建立服務提供者
description: 建立服務提供者
ms.assetid: 7da27fe2-8a57-4adb-94b2-448b6362dc33
keywords:
- Windows Media 裝置管理員，建立服務提供者
- 裝置管理員，建立服務提供者
- Windows Media 裝置管理員，程式設計手冊
- 裝置管理員，程式設計手冊
- 服務提供者程式設計指南
- Windows Media 裝置管理員程式設計指南
- 程式設計指南，建立服務提供者
- Windows Media 裝置管理員、服務提供者
- 裝置管理員，服務提供者
- 服務提供者，建立
- 建立服務提供者，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8469c3d656d151457ed818ea6b4192a3c79ed061
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969710"
---
# <a name="creating-a-service-provider"></a>建立服務提供者

服務提供者是一種元件，可做為應用程式與裝置之間的中間人。 Windows Media 裝置管理員將應用程式的要求路由傳送到服務提供者，然後負責與裝置通訊或執行要求的動作。 服務提供者通常會與驅動程式進行通訊，以啟用與裝置的通訊。 服務提供者是一種 COM 元件，可執行 Windows Media 裝置管理員所呼叫的介面。 服務提供者物件的根介面為 [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider)。 取得此介面之後，Windows Media 裝置管理員可以透過服務提供者的各種方法來取得其他介面。 服務提供者必須實作為的介面會列在 [強制和選擇性的介面](mandatory-and-optional-interfaces.md)中。 介面的階層會顯示在 [服務提供者的介面](interfaces-for-service-providers.md)中。

> [!Note]  
> 您不應該嘗試建立 MTP 服務提供者;相反地，您應該使用 MTP 服務提供者和 Microsoft 提供的驅動程式。

 

嘗試建立服務提供者之前，您應該徹底瞭解應用程式將對服務提供者進行的呼叫。 閱讀 [建立 Windows Media 裝置管理員應用程式](creating-a-windows-media-device-manager-application.md) ，以瞭解應用程式在嘗試與裝置通訊時，會在服務提供者上執行之基本工作和呼叫的一些概念。

下列清單顯示開發服務提供者的主要步驟：

1.  包含 (，並選擇性地編譯) 專案所需的標頭和程式庫檔案。 請參閱必要檔案清單中的 [服務提供者所需的程式庫和標頭](required-libraries-and-headers-for-a-service-provider.md) 。
2.  執行所有其他必要或選擇性的服務提供者介面 (查看) 的 [強制和選擇性介面](mandatory-and-optional-interfaces.md) 。 通常會依下列順序呼叫介面：
    -   [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
    -   [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider)/2
    -   [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice)
    -   [**IMDSPDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice)/2
    -   [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage)
    -   [**IMDSPStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage)/2/3
3.  在安裝期間，請確定您的服務提供者或裝置會安裝適當的登錄機碼。 這些金鑰會指定裝置參數、將服務提供者註冊為外掛程式，以及啟用裝置抵達和移除的隨插即用通知。 請參閱 [裝置參數](device-parameters.md)、 [註冊服務提供者](registering-the-service-provider.md)，以及 [為裝置啟用 PnP](enabling-pnp-for-devices.md)。
4.  在具現化類別時，請在函式中驗證服務提供者。 若要這樣做，請建立 [CSecureChannelServer](csecurechannelserver-class.md) 類別並設定憑證。 執行 [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) 介面，並呼叫先前具現化之 CSecureChannelServer 類別的方法。 請參閱 [驗證服務提供者](authenticating-the-service-provider.md) ，以瞭解如何具現化 CSecureChannelServer 類別並執行 IComponentAuthenticate 方法。
5.  Windows Media 裝置管理員會根據服務提供者是否處理隨插即用裝置，藉由呼叫 [**IMDServiceProvider2：： CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) 或 [**IMDServiceProvider：： EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices)，來查詢您的服務提供者是否有連線的裝置清單。 服務提供者必須傳回代表連線裝置的 [**IMDSPDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice) 物件清單。 如需詳細資訊，請參閱 [列舉裝置](enumerating-devices-service-provider.md) 。
6.  在處理任何呼叫之前，請先確認已建立安全通道。 執行任何動作之前，請先呼叫 [**CSecureChannelServer：： fIsAuthenticated**](/previous-versions/bb231600(v=vs.85)) 。 如果這個呼叫失敗，則傳回 WMDM \_ E \_ NOTCERTIFIED。
7.  您將需要由 Microsoft 發出的憑證/金鑰組，才能處理受 DRM 保護的資料。 如需詳細資訊，請參閱 [處理服務提供者中受保護的內容](handling-protected-content-in-the-service-provider.md) 。
8.  若要讓您的裝置自動與 Windows Media Player 同步處理，它必須滿足 [啟用 [與 Windows Media Player 同步處理](enabling-synchronization-with-windows-media-player.md)] 中所列的需求。
9.  若要讓您的裝置出現在 Windows 檔案總管中，您必須採取幾個特殊步驟， [並詳述便攜音訊播放機的需求，使其出現在 Windows 檔案總管中](requirements-for-portable-audio-players-to-appear-in-windows-explorer.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**程式設計指南**](programming-guide.md)
</dt> </dl>

 

 