---
description: 本章節中的主題將討論國際字型的基本功能。
ms.assetid: a47303b5-f49b-4d6c-b061-9d6475530e83
title: 國際字型管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4c44661b234a95abb4d40f2204382b3d074bf1d7c0bb1c68a241345211695f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083048"
---
# <a name="international-font-management"></a>國際字型管理

本章節中的主題將討論國際字型的基本功能。 如需在您的應用程式中使用國際字型技術的指示，請參閱 [國際字型列舉和選取專案](using-international-fonts-and-text.md) ，以及 [使用 ms SHELL Dlg 和 ms shell dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md)。

## <a name="font-management-infrastructure"></a>字型管理基礎結構

從 Windows 7 開始，字型管理基礎結構支援隱藏不適合用戶字型挑選清單的字型。 預設系統設定會選擇自動隱藏未針對輸入語言 ()  (鍵盤) 在作業系統系統上啟用的字型。 此外，使用者也可以選擇以手動方式隱藏字型主控台中的字型。 這項功能表示使用者不再需要面對不適當字型的長清單，對於使用非拉丁腳本的國際使用者來說特別有用。

在 Windows 7 中，沒有任何 api 可直接查詢隱藏的字型，或將字型設定為隱藏。 不過，這並不表示您無法在應用程式中利用此功能。 如果您使用 Windows [**ChooseFont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) API (字型通用對話方塊) 來立即選取字型，您將可免費取得新的行為。 Windows 7 中) 引進的新 Windows Scenic 功能區 (字型控制項也支援此行為，並提供另一個原因來「Ribbonize」您的應用程式。 如需在功能區和 **ChooseFont** 中使用字型控制項來顯示字型，同時篩選出隱藏字型的詳細資訊，請參閱 [國際字型列舉和選取](using-international-fonts-and-text.md)。

請注意，隱藏字型只會影響字型選取的 UI。 它不會影響繪圖 Api。 當您選取字型至裝置內容時，因為隱藏了字型，所以不會影響繪圖。 [**EnumFontFamiliesEx**](/windows/win32/api/wingdi/nf-wingdi-enumfontfamiliesexa)函式會繼續列舉設定為隱藏的字型。

## <a name="gdi-font-embedding-and-subsetting"></a>GDI 字型內嵌和子集

國際字型技術會利用「內嵌服務」程式庫，讓您可以將 TrueType 和 OpenType 字型組合成檔或檔案。 在檔案中內嵌字型可保證字型會出現在接收檔案的電腦上。 如需詳細資訊，請參閱 [字型內嵌參考](../gdi/font-embedding-reference.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[國際字型列舉和選取](using-international-fonts-and-text.md)
</dt> <dt>

[使用 MS Shell Dlg 和 MS Shell Dlg 2](using-ms-shell-dlg-and-ms-shell-dlg-2.md)
</dt> <dt>

[字型內嵌參考](../gdi/font-embedding-reference.md)
</dt> </dl>

 

 
