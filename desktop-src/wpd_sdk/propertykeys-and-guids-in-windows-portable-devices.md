---
description: Windows 可攜式裝置中的 PROPERTYKEYs 和 guid
ms.assetid: 3f9e9f29-37dd-47b0-997e-de81966efce2
title: Windows 可攜式裝置中的 PROPERTYKEYs 和 guid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80100b043383074f58bc27fe8e9782c4fd6d2e4f3841a28f37035f39d23cc7c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054868"
---
# <a name="propertykeys-and-guids-in-windows-portable-devices"></a>Windows 可攜式裝置中的 PROPERTYKEYs 和 guid

屬性或命令是由 PROPERTYKEY 結構所識別。 PROPERTYKEY 結構是由兩個部分所組成： GUID (fmtid 成員) 和 (pid 成員) 的 DWORD。 GUID 部分可用來指出屬性或命令所屬的類別 (也就是屬於相同分類的相關屬性，以及屬於相同類別的相關命令;因此，它們會有相同的 fmtid) 。 DWORD 部分表示屬性或命令識別碼，用來區別屬性或命令類別中的個別屬性或命令 (也就是說，相同類別目錄中屬性或命令的 pid 值會) 不同。

本檔的參考章節說明 WPD 定義的所有 PROPERTYKEY 值;這些值會對應至命令、屬性和資源。 如果您建立自訂 PROPERTYKEY 值，您應該定義新的 **GUID** 類別目錄。請勿重複使用 WPD **GUID** 值，或您與現有和未來 WPD 指定的 PROPERTYKEYs 有衝突的風險。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**應用程式總覽**](application-overview.md)
</dt> <dt>

[**命令**](commands.md)
</dt> <dt>

[**物件格式 Guid**](object-format-guids.md)
</dt> <dt>

[**屬性和屬性**](properties-and-attributes.md)
</dt> <dt>

[**物件的需求**](requirements-for-objects.md)
</dt> </dl>

 

 



