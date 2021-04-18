---
title: IWMProfile 介面
description: IWMProfile 介面是設定檔物件的主要介面。
ms.assetid: 00f28d6b-d27d-4268-960e-c8ea25e5359e
keywords:
- IWMProfile 介面 windows 媒體格式
- IWMProfile 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IWMProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- wmsdkidl.h
ms.openlocfilehash: f814df820bd50a36abf2ee8e453549f46c9c5c9e
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "106966069"
---
# <a name="iwmprofile-interface"></a>IWMProfile 介面

**IWMProfile** 介面是 [*設定檔*](wmformat-glossary.md)物件的主要介面。 設定檔物件是用來設定自訂設定檔。 您可以使用 **IWMProfile** 來建立、刪除或修改串流設定物件和相互排除物件。 您也可以設定和取得設定檔的一般資訊。 若要存取設定檔物件的所有功能，您應該使用繼承自 **IWMProfile** 和 [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)的 [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)。

**IWMProfile** 也可以透過 reader 物件來存取，您可以在其中使用它來取得讀取器中所載入之檔案的資料流程相關資訊。 從讀取器存取 **IWMProfile** 時，您可以對設定檔進行變更，但不能將任何變更儲存到檔案中。 使用現有檔案的設定檔作為新設定檔的基礎通常很方便。 同步讀取器以與讀取器相同的方式支援 **IWMProfile** 。

透過讀取器或同步讀取器取得的設定檔資訊不是來自 prx 檔案。 讀取器會使用 ASF 檔案中的資訊來組合串流設定。 因此，某些設定檔資訊（例如名稱和描述）無法透過讀取器使用。

有幾種方式可以取得 **IWMProfile** 介面的指標。 配置檔案管理員有方法可建立新的設定檔，以及存取現有的設定檔。 所有這些方法都會設定 **IWMProfile** 指標。 讀取檔案時，可以藉由呼叫任何讀取器介面的 **QueryInterface** 方法來取得 **IWMProfile** 的指標。 同樣地，同步讀取器物件的任何介面都可以透過呼叫 **QueryInterface**[**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)來取得指標。

## <a name="members"></a>成員

**IWMProfile** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IWMProfile** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWMProfile** 介面具有這些方法。



| 方法                                                                  | 描述                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)             | 將相互排除物件新增至設定檔。<br/>                                   |
| [**AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream)                               | 將資料流程新增至設定檔。<br/>                                                    |
| [**CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | 建立設定檔的相互排除物件。<br/>                               |
| [**CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)                   | 建立設定檔的串流設定物件。<br/>                           |
| [**GetDescription**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getdescription)                     | 捕獲設定檔的描述。<br/>                                        |
| [**GetMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | 從設定檔抓取相互排除物件。<br/>                            |
| [**GetMutualExclusionCount**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount)   | 捕獲設定檔中互斥物件的數目。<br/>                 |
| [**GetName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getname)                                   | 捕獲設定檔的名稱。<br/>                                               |
| [**GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                               | 使用自設定檔中的索引編號來抓取資料流程。<br/>                     |
| [**GetStreamByNumber**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber)               | 使用來自設定檔的資料流程數目來抓取資料流程。<br/>            |
| [**GetStreamCount**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)                     | 捕獲設定檔中的資料流程數目。<br/>                                  |
| [**GetVersion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getversion)                             | 捕獲設定檔中 Microsoft Windows Media Services 的版本號碼。<br/> |
| [**ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)                     | 啟用要包含在設定檔中的串流設定變更。<br/>    |
| [**RemoveMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removemutualexclusion)       | 從設定檔中移除相互排除物件。<br/>                              |
| [**RemoveStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestream)                         | 從設定檔移除資料流程。<br/>                                               |
| [**RemoveStreamByNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestreambynumber)         | 從設定檔移除資料流程。<br/>                                               |
| [**SetDescription**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setdescription)                     | 指定設定檔的描述。<br/>                                        |
| [**SetName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setname)                                   | 指定設定檔的名稱。<br/>                                               |



 

如需有關使用此介面的 QueryInterface 方法可取得哪些介面的詳細資訊，請參閱此介面執行所在物件的主題。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**介面**](interfaces.md)
</dt> <dt>

[**IWMProfileManager 介面**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**設定檔管理員物件**](profile-manager-object.md)
</dt> <dt>

[**讀取器物件**](reader-object.md)
</dt> <dt>

[**同步讀取器物件**](synchronous-reader-object.md)
</dt> <dt>

[**使用設定檔**](working-with-profiles.md)
</dt> </dl>

 

