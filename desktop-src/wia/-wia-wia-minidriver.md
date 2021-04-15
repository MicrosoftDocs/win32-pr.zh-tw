---
description: 應用程式會將 Windows 映像取得 (WIA) 裝置視為 IWiaItem 或 IWiaItem2 物件的階層式樹狀結構，其中根專案代表裝置本身。
ms.assetid: ae4ded93-09be-4caa-ad6e-1a9071fdb4b6
title: WIA 迷你驅動程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5aadaf55cfe2e8102d4e0e02cf9787b9696e327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511601"
---
# <a name="wia-minidriver"></a>WIA 迷你驅動程式

應用程式會將 Windows 映像取得 (WIA) 裝置視為 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 或 [**IWiaItem2**](-wia-iwiaitem2.md) 物件的階層式樹狀結構，其中根專案代表裝置本身。 WIA 裝置可同時由一個以上的應用程式使用。 因此，每個應用程式的 **IWiaItem** 或 **IWiaItem2** 物件檢視都必須與另一個應用程式的視圖無關。 這可透過兩個不同的專案物件來完成。 驅動程式會使用 WIA 驅動程式服務方法來建立 [IWiaDrvItem 介面](https://msdn.microsoft.com/library/ms793976.aspx) 物件的驅動程式專案樹狀結構，也稱為驅動程式專案。 這些是驅動程式用來表示每個驅動程式內部專案的全域物件。 當應用程式建立 **IWiaItem** 或 **IWiaItem2** 物件 (也稱為應用程式專案) 時，此物件會連結至驅動程式專案樹狀結構中驅動程式的對應 [IWiaDrvItem 介面](https://msdn.microsoft.com/library/ms793976.aspx) 。 參考計數會在 [IWiaDrvItem 介面](https://msdn.microsoft.com/library/ms793976.aspx) 物件上保留，且受限於下列規則：

-   當驅動程式將 [IWiaDrvItem 介面](https://msdn.microsoft.com/library/ms793976.aspx) 物件加入至驅動程式專案樹狀結構時， [IWiaDrvItem 介面](https://msdn.microsoft.com/library/ms793976.aspx) 物件的參考計數會遞增。 這通常會在 IWiaMiniDrv 期間發生 [：:D rvinitializewia](https://msdn.microsoft.com/library/ms794097.aspx) 或處理 WIA \_ CMD \_ SYNCHRONIZE 命令時。
-   當驅動程式從驅動程式專案樹狀結構中移除 [IWiaDrvItem 介面](https://msdn.microsoft.com/library/ms793976.aspx) 物件時， [IWiaDrvItem 介面](https://msdn.microsoft.com/library/ms793976.aspx) 物件的參考計數會減少，並標示 [IWiaDrvItem 介面](https://msdn.microsoft.com/library/ms793976.aspx) 物件，使其無法再次存取裝置。 當裝置中斷連線或刪除專案時，通常會發生這種情況。 即使已從驅動程式專案樹狀結構中移除對應的 [IWiaDrvItem 介面](https://msdn.microsoft.com/library/ms793976.aspx)物件，應用程式仍能從 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)或 [**IWiaItem2**](-wia-iwiaitem2.md)物件讀取屬性。
-   建立 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 或 [**IWiaItem2**](-wia-iwiaitem2.md) 物件時，它會連結至對應的 [IWiaDrvItem 介面](https://msdn.microsoft.com/library/ms793976.aspx) 物件。 [IWiaDrvItem 介面](https://msdn.microsoft.com/library/ms793976.aspx)物件的參考計數會遞增。
-   釋放 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 或 [**IWiaItem2**](-wia-iwiaitem2.md) 物件時，會中斷其對應 [IWiaDrvItem 介面](https://msdn.microsoft.com/library/ms793976.aspx) 物件的連結，並減少 [IWiaDrvItem 介面](https://msdn.microsoft.com/library/ms793976.aspx) 物件的參考計數。
-   如果 [IWiaDrvItem 介面](https://msdn.microsoft.com/library/ms793976.aspx) 物件的參考計數變成零，則會刪除 [IWiaDrvItem 介面](https://msdn.microsoft.com/library/ms793976.aspx) 物件。 這適用于所有 [IWiaDrvItem 的介面](https://msdn.microsoft.com/library/ms793976.aspx) 物件，包括根專案。 [IWiaDrvItem 介面](https://msdn.microsoft.com/library/ms793976.aspx)物件的參考計數只有在沒有任何應用程式專案參考時，才會變成零，而且不再連結至驅動程式專案樹狀結構。

使用此參考計數配置時，許多 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 或 [**IWiaItem2**](-wia-iwiaitem2.md) 物件可以連結至一個 [IWiaDrvItem 介面](https://msdn.microsoft.com/library/ms793976.aspx) ，而不會受到干擾。 由於每個 **IWiaItem** 或 **IWiaItem2** 都包含它自己的屬性儲存空間，因此即使在刪除專案之後，應用程式還是可以繼續讀取專案屬性，但不需要存取裝置的作業也會成功。 因為專案屬性儲存在 **IWiaItem** 或 **IWiaItem2** 物件中，所以在資料傳輸之前，驅動程式必須將 **IWiaItem** 或 **IWiaItem2** 物件的屬性設定為裝置。

 

 



