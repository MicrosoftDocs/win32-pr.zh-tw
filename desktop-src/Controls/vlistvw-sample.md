---
title: VListVW 範例
ms.assetid: 5e1d13a6-ae11-4729-b0fc-0a1620cf0738
description: 深入瞭解： VListVW 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7445f83d08641179f9ee0e5b3aeeee5a613f1f6b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970110"
---
# <a name="vlistvw-sample"></a>VListVW 範例

本主題說明 VListVW 範例程式碼範例。 它包含下列區段：

-   [說明](#description)
-   [最低需求](#minimum-requirements)
-   [下載範例](#downloading-the-sample)
-   [建立範例](#building-the-sample)
-   [相關主題](#related-topics)

## <a name="description"></a>Description

VListVW 範例示範如何在應用程式中執行簡單的虛擬清單視圖控制項。 虛擬清單-view 控制項是具有 **lvs) \_ OWNERDATA** 樣式的標準清單視圖控制項。 此範例會建立「虛擬」保存100000專案的清單視圖控制項。 絕不會實際新增專案。 相反地，虛擬清單視圖控制項會「告知」它包含 [**LVM \_ SETITEMCOUNT**](lvm-setitemcount.md) 訊息的專案數目。 當需要繪製專案時，清單視圖控制項會查詢父視窗，以取得 [LVN \_ GETDISPINFO](lvn-getdispinfo.md) 通知的顯示資訊。

## <a name="minimum-requirements"></a>最低需求



| 產品          | 版本                               |
|------------------|---------------------------------------|
| DLL              | comctl32.dll 版本4.70             |
| 作業系統 | Windows 95、Microsoft Windows NT 3.51 |



 

## <a name="downloading-the-sample"></a>下載範例

VListVW 範例可在 github 上的 [Windows 傳統範例存放庫](https://github.com/microsoft/Windows-classic-samples)中取得。 您可以在[這裡](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)找到清單視圖控制項專案範例

 

## <a name="building-the-sample"></a>建立範例

若要使用命令提示字元建立範例：

1.  開啟 [命令提示字元] 視窗，並流覽至專案目錄。
2.  輸入 `msbuild [project file]`。

若要使用 Visual Studio 建立範例：

1.  開啟 Windows 檔案總管並流覽至專案目錄。
2.  按兩下 vcproj 檔案的圖示，在 Visual Studio 中開啟專案。
3.  從 [ **組建** ] 功能表中，選取 [ **建立方案** ] 來建立方案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 List-View 控制項](list-view-controls-overview.md)
</dt> </dl>

 

 




