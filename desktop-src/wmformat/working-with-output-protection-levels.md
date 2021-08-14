---
title: 使用輸出保護層級
description: 使用輸出保護層級
ms.assetid: ec5982cd-0b87-4081-98e2-ab2d102a36d8
keywords:
- 'Windows媒體格式 SDK，輸出保護層級 (OPL) '
- Windows媒體格式 SDK，保護層級
- 'Advanced Systems Format (ASF) ，輸出保護層級 (OPL) '
- 'ASF (Advanced Systems Format) ，輸出保護層級 (OPL) '
- Advanced Systems Format (ASF) 、保護等級
- ASF (Advanced Systems Format) ，保護等級
- Advanced Systems Format (ASF) 、多重授權
- ASF (Advanced Systems Format) 、多重授權
- '數位版權管理 (DRM) ，輸出保護層級 (OPL) '
- 'DRM (數位版權管理) ，輸出保護層級 (OPL) '
- 數位版權管理 (DRM) ，保護等級
- DRM (數位版權管理) ，保護等級
- '數位版權管理 (DRM) ， (OPL 評估輸出保護層級) '
- 'DRM (數位版權管理) ， (OPL 評估輸出保護層級) '
- 數位版權管理 (DRM) ，多個授權
- DRM (數位版權管理) 、多重授權
- '輸出保護層級 (OPL) '
- 'OPL (輸出保護層級) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2888891e50ec90e784bf6f4420637544854a9b600b5538e9655bc6d3028f76d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697712"
---
# <a name="working-with-output-protection-levels"></a>使用輸出保護層級

使用 Windows 媒體版權管理員 10 SDK 建立的授權可以使用輸出保護層級 (OPLs) 來指定動作限制。 OPLs 可讓授權建立者只允許在具有特定技術的裝置上執行某些動作。 使用 OPLs 的優點是，您在建立比舊版更多的授權時，會獲得更多的彈性。 此外，OPLs 可哥擴充以容納未來的技術。 您可以使用 [**IWMDRMReader2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2) 介面的方法，在您的應用程式中支援這類授權。

若要讀取由指定 OPLs 的授權所保護的檔案，您必須檢查 OPL 是否有想要的動作。 授權中的 OPL 必須允許您的應用程式所使用的輸出技術。 例如，某些受保護音訊的授權可能會要求您使用安全音訊路徑來播放。

## <a name="configuring-the-reader-to-evaluate-output-protection-levels"></a>設定讀取器來評估輸出保護層級

您必須先呼叫 [**IWMDRMReader2：： SetEvaluateOutputLevelLicenses**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-setevaluateoutputlevellicenses) 方法，並傳遞 **TRUE** 作為 *FEvaluate* 參數，才能檢查 OPLs 中載入的檔案。 如果您沒有呼叫這個方法，您的應用程式就看不到需要 OPLs 的授權。

## <a name="evaluating-copy-output-protection-levels"></a>評估複製輸出保護層級

若要取得複製動作的輸出保護層級，請呼叫 [**IWMDRMReader2：： GetCopyOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getcopyoutputlevels) 方法。 您從呼叫收到的資料會儲存在 [**DRM \_ 複製 \_ OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl) 結構中。 此結構包含基底輸出保護層級，以指定授權中複製動作的最小輸出層級。 不過，DRM \_ 複製 \_ OPL 結構也包含兩個技術識別碼清單：一個適用于以較低的 OPL 分級的所允許技術，另一個則適用于評等等於或高於基底 OPL 但受授許可權制的技術。 您必須檢查包含與排除專案，以確定授權允許您的應用程式所使用的技術。

## <a name="evaluating-play-output-protection-levels"></a>評估播放輸出保護層級

若要取得播放動作的輸出保護層級，請呼叫 [**IWMDRMReader2：： GetPlayOutputLevels**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-getplayoutputlevels) 方法。 您從呼叫收到的資料會儲存在 [**DRM \_ PLAY \_ OPL**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl) 結構中。 結構包含數個其他結構。 播放動作的基底輸出保護層級會以 Drm 的 [**\_ 最小 \_ 輸出 \_ 保護 \_ 層級**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels)結構儲存 (**drm \_ play \_ OPL**) 的 **minOPL** 成員，其定義以各種格式播放內容所需的最小 OPL。 您必須檢查成員是否有應用程式傳遞的輸出格式類型。

**DRM \_ PLAY \_ OPL** 結構定義了兩種限制：需要向下取樣，以及允許的影片輸出保護識別碼。

必要的向下取樣定義為 (**DRM \_ PLAY \_ OPL** 的 **oplIdDownsample** 成員的輸出技術識別碼清單) 這種情況下，只有在內容第一次向下取樣時，才可以接收內容以供播放。

允許的影片輸出保護識別碼會定義為影片輸出技術的清單，其中包含每個的設定資訊。

## <a name="handling-multiple-licenses"></a>處理多個授權

某些檔案可能會在本機授權存放區中有多個相關聯的授權。 當您針對正在讀取的檔案評估 OPLs 時，您可以藉由呼叫 [**IWMDRMReader2：： TryNextLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader2-trynextlicense) 方法來檢查是否有額外的授權。 您應繼續嘗試授權，直到找到允許您想要執行之動作的授權，或直到 TryNextLicense 傳回 DRM \_ S \_ FALSE，這表示沒有其他授權。

在某些情況下，檔案可能會有相關聯的授權，需要您的應用程式無法支援的 OPL。 在這種情況下，請務必檢查是否有額外的授權，因為可能存在未指定 OPLs 的授權。

**注意** 此 SDK 的 x64 版本不支援 DRM。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**啟用 DRM 支援**](enabling-drm-support.md)
</dt> <dt>

[**IWMDRMReader2 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader2)
</dt> </dl>

 

 




