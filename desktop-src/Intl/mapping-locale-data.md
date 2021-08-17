---
description: NLS 包含許多 API 函式，可讓您的應用程式用來對應地區設定識別碼與地區設定名稱之間的地區設定資料，以及列出中立的地區設定。
ms.assetid: 01bc261d-dfee-430e-86c9-cfafe82856c8
title: 對應地區設定資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1576844f13dda80a6b9d754fc807ef8a35514dcfedd88dc04cf233cfb2a1bfb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147190"
---
# <a name="mapping-locale-data"></a>對應地區設定資料

NLS 包含許多 API 函式，可讓您的應用程式用來對應 [地區設定識別碼](locale-identifiers.md) 與 [地區設定名稱](locale-names.md)之間的地區設定資料，以及列出中立的地區設定。 本主題討論如何在 Windows vista 和更新版本上，以及在預先 Windows 的 Vista 作業系統上使用這些功能 (有時候稱為「下層系統」 ) 。

## <a name="map-locale-data-on-windows-vista-and-later"></a>Windows Vista 和更新版本上的地圖地區設定資料

NLS 提供數個地區設定對應函式，可供您開發用來在 Windows Vista 和更新版本上執行的應用程式使用。 它也包含您的應用程式可用來列舉中性地區設定的函式。

**使用標準轉換函數進行資料對應**

若要在地區設定名稱和地區設定識別碼之間進行對應，您的應用程式可以呼叫 [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) 函數。 應用程式會使用 [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) ，在地區設定識別碼和地區設定名稱之間進行對應。

**列出中性地區設定**

若要列舉 Windows 7 和更新版本的中性地區設定，您的應用程式可以呼叫 [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) ，並將 *dwFlags* 設定為 [**地區設定 \_ NEUTRALDATA**](locale-neutraldata.md)。 它也可以使用 [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) ，並將 *LCType* 設定為 [**地區設定 \_ INEUTRAL**](locale-ineutral.md)。

## <a name="map-locale-data-on-pre-windows-vista-operating-systems"></a>在預先 Windows 的 Vista 作業系統上對應地區設定資料

NLS 包含 (DLL) 的直接程式庫，可用於您開發的應用程式，以在預先 Windows Vista 作業系統上執行。 DLL 支援轉換和列出資料對應的函數。

> [!Note]  
> 只在 Windows Vista 和更新版本上執行的應用程式不應使用下層對應或清單功能。

 

**使用早期轉換函數進行資料對應**

以下層系統為目標的應用程式可以呼叫 [**DownlevelLCIDToLocaleName**](downlevellcidtolocalename.md) 函式，將地區設定識別碼轉換為地區設定名稱。 如果需要將地區設定名稱轉換成地區設定識別碼，則應該呼叫 [**DownlevelLocaleNameToLCID**](downlevellocalenametolcid.md)。

**使用下層清單函式來列舉中性地區設定**

您的應用程式應該呼叫 [**DownlevelGetParentLocaleLCID**](downlevelgetparentlocalelcid.md) ，以取得地區設定的父系地區設定識別碼。 如果應用程式需要取得地區設定之父系的地區設定名稱，則應該呼叫 [**DownlevelGetParentLocaleName**](downlevelgetparentlocalename.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用國家語言支援](using-national-language-support.md)
</dt> <dt>

[地區設定識別碼](locale-identifiers.md)
</dt> <dt>

[地區設定名稱](locale-names.md)
</dt> </dl>

 

 



