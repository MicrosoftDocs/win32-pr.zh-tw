---
title: 安全內容提供者的介面
description: 安全內容提供者的介面
ms.assetid: a3eecdb8-55a9-46e3-95d1-0fb9bd59f393
keywords:
- Windows媒體裝置管理員、受 DRM 保護的內容
- 裝置管理員，受 DRM 保護的內容
- 程式設計參考，受 DRM 保護的內容
- Windows 媒體裝置管理員的參考，受 DRM 保護的內容
- 受 DRM 保護的內容
- 'Windows媒體裝置管理員，安全內容提供者 (SCP) '
- '裝置管理員， (SCP 的安全內容提供者) '
- '程式設計參考，安全內容提供者 (SCP) '
- 'Windows 媒體裝置管理員、安全內容提供者 (SCP 的參考) '
- " (SCP) 的安全內容提供者"
- 'SCP (保護內容提供者) '
- WindowsMedia 裝置管理員、SCP 介面
- 裝置管理員，SCP 介面
- 程式設計參考，SCP 介面
- Windows 媒體裝置管理員、SCP 介面的參考
- SCP 介面，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a80b74cfc50fb6dcf328379c5c46696dc2ee097e2ed5c2507a2a4f14676efd85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119247338"
---
# <a name="interfaces-for-secure-content-providers"></a>安全內容提供者的介面

 (SCP) 的安全內容提供者是外掛程式元件，可讓 Windows 媒體裝置管理員從受 DRM 保護的內容傳送和要求許可權資訊。 Microsoft 提供的 SCP 元件可以處理受 DRM 保護的 WMA 和 WMV 檔案。 如果您的裝置或應用程式將使用其他格式的受 DRM 保護內容，它應該藉由執行所有這些介面來建立 SCP 元件。 否則，您將不需要使用這些介面。



| 介面                                                  | 描述                                                                                                                                                                                                                                          |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISCPSecureAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate)   | 安全內容提供者的主要介面。                                                                                                                                                                                                |
| [**ISCPSecureAuthenticate2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureauthenticate2) | 藉由提供取得會話物件的方法來擴充 **ISCPSecureAuthenticate** 。                                                                                                                                                                       |
| [**ISCPSecureExchange**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange)           | 用來交換與內容相關聯的受保護內容和許可權。                                                                                                                                                                                 |
| [**ISCPSecureExchange2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange2)         | 藉由提供新版本的 **TransferContainerData** 方法來擴充 **ISCPSecureExchange** 。                                                                                                                                                   |
| [**ISCPSecureExchange3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)         | 藉由提供改良的資料交換效能以及傳送完成的回呼方法，來擴充 **ISCPSecureExchange2** 。                                                                                                                            |
| [**ISCPSecureQuery**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery)                 | Windows 媒體裝置管理員查詢，以決定受保護內容的擁有權。                                                                                                                                                                   |
| [**ISCPSecureQuery2**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2)               | 透過可判斷安全內容提供者是否負責內容的功能來擴充 **ISCPSecureQuery** ，如果是的話，請提供 URL 來更新撤銷的元件，並判斷哪些元件已被撤銷。 |
| [**ISCPSecureQuery3**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery3)               | 擴充 **ISCPSecureQuery2** ，方法是提供一組新方法來取得明確通道的許可權並進行決策。                                                                                                                     |
| [**ISCPSession**](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsession)                         | 為多項作業提供有效率的一般狀態管理。                                                                                                                                                                                  |



 

 

 




