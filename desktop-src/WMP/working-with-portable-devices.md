---
title: 使用可攜式裝置
description: 使用可攜式裝置
ms.assetid: 145ede07-a23b-486b-a561-9c87a48b72a8
keywords:
- Windows Media Player，可攜式裝置
- Windows Media Player 物件模型，可攜式裝置
- 物件模型，可攜式裝置
- Windows Media Player ActiveX 控制、可攜式裝置
- ActiveX 控制，可攜式裝置
- Windows Media PlayerMobile ActiveX control、可攜式裝置
- Windows Media Player行動裝置、可攜式裝置
- 可攜式裝置，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34cbff16b293ac4ab438c1b018608497d2a61cdfa6fb727332d5b50a27de313c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117745504"
---
# <a name="working-with-portable-devices"></a>使用可攜式裝置

本節說明如何使用遠端 Windows Media Player ActiveX 控制項來處理可攜式裝置。

本節中的程式碼範例會使用 Active Template Library (ATL) 類別，例如 **CComPtr**。

## <a name="included-headers"></a>包含的標頭

若要使用本節中的程式碼，請包含下列標頭：


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"
```



## <a name="iwmpplayer-pointer"></a>IWMPPlayer 指標

**IWMPPlayer** 指標會儲存在成員變數中。


```C++
CComPtr<IWMPPlayer> m_spPlayer;
```



## <a name="devices-are-stored-in-an-array"></a>裝置會儲存在陣列中

範例程式碼會存取在專案標頭中宣告的下列成員變數：


```C++
IWMPSyncDevice **m_ppWMPDevices; // Points to the custom device array.
```



裝置計數會儲存在成員變數中。


```C++
int m_cDevices; // Count of devices.
```



## <a name="retrieving-a-device-pointer"></a>正在抓取裝置指標

使用與下列類似的程式碼，透過其陣列索引來抓取特定裝置的指標：


```C++
CComPtr<IWMPSyncDevice> spSyncDevice(m_ppWMPDevices[lIndex]);
```



請注意，上述範例中所顯示的索引不是裝置的合作關係索引。 它是裝置在自訂陣列中的索引。

## <a name="cleaning-up"></a>清理

這些範例會使用下列函式釋放裝置陣列中的記憶體，並釋放介面指標：


```C++
void CMainDlg::FreeDeviceArray()
{
    if(m_ppWMPDevices)
    {
        for(long i = 0; i < m_cDevices; i++)
        {
            m_ppWMPDevices[i]->Release();
        }
 
        delete[] m_ppWMPDevices;
        m_ppWMPDevices = NULL;        
    }
}
```



## <a name="devices-are-displayed-in-a-list-box"></a>裝置會顯示在清單方塊中

GetSelectedDeviceIndex 函式會使用下列程式碼，傳回使用者在清單方塊中選取之裝置的索引：


```C++
long CMainDlg::GetSelectedDeviceIndex()
{
    return (long)SendMessage(GetDlgItem(IDC_DEVICES), LB_GETCURSEL, 0, 0);
}
```



## <a name="user-interface-state-is-managed-by-a-single-function"></a>消費者介面狀態是由單一函式管理

SetUIState 函數會管理使用者介面。


```C++
SetUIState(UIState 
NewState, BOOL 
bConnected)
```



此函數的詳細資料與本節中的討論無關，但請注意，此函式會執行工作，例如啟用或停用控制項，以及變更使用者介面中的顯示文字。

UIState 列舉的定義如下：


```C++
enum UIState
{
    Partnership,
    NoPartnership,
    Synchronizing
};
```



*BConnected* 參數會指定是否要為連線的裝置設定使用者介面 (TRUE 表示裝置已連線) 。 *NewState* 和 *bConnected* 參數會傳達函數執行其工作所需的資訊。

下列各節提供範例程式碼的說明：

-   [列舉裝置](enumerating-devices.md)
-   [正在抓取裝置屬性](retrieving-device-attributes.md)
-   [顯示同步處理進度](showing-synchronization-progress.md)
-   [管理同步播放清單](managing-synchronization-playlists.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**播放機控制指南**](player-control-guide.md)
</dt> </dl>

 

 




