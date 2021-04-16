---
title: 取得必要的 DRM 程式庫
description: 取得必要的 DRM 程式庫
ms.assetid: 7bd13b77-439e-40cf-99e8-b359247da74d
keywords:
- Windows Media Format SDK，取得必要的 DRM 程式庫
- Advanced Systems Format (ASF) ，取得必要的 DRM 程式庫
- ASF (Advanced Systems Format) ，取得必要的 DRM 程式庫
- 數位版權管理 (DRM) ，取得必要的程式庫
- DRM (數位版權管理) ，取得必要的程式庫
- 數位版權管理 (DRM) ，組建資訊
- DRM (數位版權管理) ，組建資訊
- 數位版權管理 (DRM) ，調試資訊
- DRM (數位版權管理) ，調試資訊
- 偵測 DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5c124c1e7edf0bba736b9dd392e852aac97e96
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383130"
---
# <a name="obtaining-the-required-drm-library"></a>取得必要的 DRM 程式庫

若要建立或播放受 DRM 保護的數位媒體檔案，您的應用程式必須連結至 Microsoft 以二進位格式提供的靜態程式庫。 此程式庫有時稱為存根程式庫或「stublib」，它可唯一識別您的應用程式。

在此檔中，DRM 程式庫稱為「WMStubDRM .lib」。 您所收到的程式庫名稱將包含識別編號。 若要取得此程式庫，您必須簽署 Microsoft 的授權合約。 合約條款可能會根據您是否要求評估授權或生產授權而有所不同。 如需 DRM 授權流程的詳細資訊，請參閱 [Microsoft](https://www.microsoft.com/licensing/default)網站上的 Windows Media 授權表單。

您收到的程式庫具有 DRM 安全性等級，這取決於您輸入的授權合約類型。 DRM 授權可以在指定的安全性層級下，限制具有 DRM 元件的應用程式存取檔案內容。 此安全性層級與 DRM 的個人化層級不同，它與輸出保護層級的任何數值 (OPLs) 無關。 下表顯示不同播放程式和可攜式裝置的 DRM 安全性層級範例。



| 安全性層級 | 播放機和可攜式裝置                                                                                                                                                                                                                                                                                                   | 範例                                                                                                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 150            | 不支援 Windows Media DRM 的裝置。 將內容傳輸到這類裝置時，會移除 DRM 保護。                                                                                                                                                                                                         | 支援 Windows Media 內容但不受保護內容的裝置                                                                                                                       |
| 1,000          | 以 Windows Media Format 9.5 SDK 或更早版本為基礎的播放機應用程式，不符合等級2000的其他需求。以 Windows Media 可攜式裝置 DRM v1 為基礎的裝置。<br/> 以 Windows CE 4.2 和更新版本為基礎的裝置。<br/>                                                                       | Windows Media Player 6.4，Windows Media Player 7Portable 支援 Windows Media 可攜式裝置 DRM v1 的媒體裝置。<br/>                                                             |
| 2,000          | 以 Windows Media Format 9 系列 SDK 或更新版本為基礎的播放程式應用程式，並遵循比層級1000的應用程式更嚴格的內容保護指導方針。以 Windows Media DRM 10 作為可攜式裝置的裝置為基礎。<br/> 以 Windows Media DRM 10 為基礎的裝置，適用于網路裝置。<br/> | 適用于可攜式裝置的 Windows Media Player 9 系列和 laterPortable 媒體裝置支援 Windows Media DRM 10<br/> 以 Windows Mobile 為基礎的便攜 Media Center 裝置<br/> |



 

## <a name="build-and-debugging-information"></a>組建和調試資訊

當您連結到 WMStubDRM 時，請不要連結至 wmvcore .lib。 如果應用程式連結至這兩個程式庫，DRM 元件將無法正常運作。

DRM 元件中的使用者中斷點可防止應用程式的 debug 和 release 版本在偵錯工具內執行時存取受保護的內容。 若要針對應用程式中的 DRM 相關函式進行疑難排解，您必須撰寫自己的追蹤常式，將 **HRESULT** 值之類的資訊儲存到某個位置，例如記錄檔。

如果您嘗試在已安裝 (的 SDK bits 的偵測版本的系統上執行應用程式的發行版本，或使用另一種方式進行) ，您將會在播放 DRM 版本7內容時遇到堆積錯誤。 請務必透過 debug SDK bits 來執行 debug 應用程式，並透過版本位發行應用程式。 如果您以個別的 DRM 元件執行 SDK 的偵錯工具版本，則會發生相同的問題， (一律為發行組建) 。

**附注** 此 SDK 的 x64 版本不支援 DRM。

與 Windows Media Format 9.5 SDK 相關聯的 WMStubDRM .lib 檔案只能搭配 Microsoft Visual Studio .NET 2003 的元件使用。 如果您使用較舊版本的存根程式庫，則不會有任何新的限制可供使用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**啟用 DRM 支援**](enabling-drm-support.md)
</dt> </dl>

 

 





