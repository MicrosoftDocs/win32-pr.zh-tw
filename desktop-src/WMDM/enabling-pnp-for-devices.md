---
title: 啟用裝置的 PnP
description: 啟用裝置的 PnP
ms.assetid: 510237a9-2b74-4c2e-ad45-3f45117289a6
keywords:
- Windows Media 裝置管理員、PnP 裝置
- 裝置管理員，PnP 裝置
- 程式設計指南，PnP 裝置
- 服務提供者、PnP 裝置
- 建立服務提供者，PnP 裝置
- PnP 裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44c7ccdfd29453c1ab28e970c1b054d1278e620
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839775"
---
# <a name="enabling-pnp-for-devices"></a>啟用裝置的 PnP

Windows Media 裝置管理員可監視通告便攜音訊播放機裝置介面之裝置的抵達和移除通知。 在這類裝置抵達時，Windows Media 裝置管理員會查詢名為 *WMDMSPCLSID* 的裝置參數，以取得負責此裝置之服務提供者的類別識別碼。 Windows Media 裝置管理員會在此服務提供者上呼叫 [**IMDServiceProvider2：： CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) 來建立裝置物件，該物件會以 [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) 物件的形式公開給應用程式。

服務提供者可以處理 PnP 裝置或非 PnP 裝置;它無法處理這兩種類型。

若要讓裝置使用上述機制 (並因此啟用 Windows Media 裝置管理員應用程式) 下裝置的抵達和移除通知，必須符合下列需求：

-   此裝置的設備磁碟機必須通告 Windows Media 裝置管理員便攜音訊播放機裝置介面。 此裝置介面的 GUID 定義如下：

    ```
    {0xf33fdc04, 0xd1ac, 0x4e8e, {0x9a, 0x30, 0x19, 0xbb, 0xd4, 0xb1, 0x8, 0xae} }
    ```

    

    > [!Note]  
    > 如果裝置通告磁片區介面 (定義為 \_) winioctl 中的 VolumeClassGuid 或 GUID DEVINTERFACE 磁片區，則裝置不應通告此介面 \_ 。 如果裝置通告磁片區介面，則在 Windows Media 裝置管理員下，它已啟用 PnP。

     

    -AND/OR-

    您必須在子機碼 HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows Media 裝置管理員 \\ KnownDevices 中建立服務提供者的新登錄子機碼。 此金鑰應該有您服務提供者的名稱，而且必須具有下列兩個 Reg \_ SZ 值專案：

    ```
    DeviceInterface         {25DBCE51-6C8F-4A72-8A6D-B54C2B4FC835}
    WMDMSPCLSID             {067B4B81-B1EC-489F-B111-940EBDC44EBE}
    ```

    

-   裝置必須具有名為 WMDMSPCLSID 的裝置參數。 此參數的值應該設定為字串形式的服務提供者 CLSID。 如需裝置參數的詳細資訊，請參閱 [裝置參數](device-parameters.md)。

    > [!Note]  
    > 參數值必須是 CLSID，而不是服務提供者的 ProgID。

     

-   此裝置的服務提供者必須執行 IMDServiceProvider2 介面。
-   HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ Windows Media 裝置管理員外掛程式 SP sp 名稱下的服務提供者金鑰 \\ \\ \\ 必須包含下列 DWORD 值
    ```
    PnPAware    1
    ```

    

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立服務提供者**](creating-a-service-provider.md)
</dt> </dl>

 

 




