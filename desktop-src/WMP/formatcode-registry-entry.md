---
title: FormatCode 登錄專案
description: FormatCode 登錄專案
ms.assetid: cc444eaa-6898-48ab-9573-9e7d5e25d6db
keywords:
- Windows Media Player，FormatCode 登錄專案
- Windows Media Player、副檔名
- Windows Media Player，登錄
- 登錄、副檔名
- 登錄，FormatCode 專案
- 登錄，Windows Media Player 的設定
- 副檔名登錄設定
- FormatCode 登錄專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2318d32e9d7a08a2ae23b24e7acd2674b9eecb2
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104185481"
---
# <a name="formatcode-registry-entry"></a>FormatCode 登錄專案

當 Windows Media Player 遇到自訂副檔名時，它會尋找符合擴充功能的登錄子機碼。 此子機碼描述于副檔名登錄 [設定](file-name-extension-registry-settings.md)中。 其中一個可出現在擴充功能子機碼底下的登錄專案是 **FormatCode** 專案。

**FormatCode** 登錄專案會針對具有自訂延伸模組的檔案，指定 (MTP) 格式代碼的媒體傳輸通訊協定。 **FormatCode** 登錄專案具有下列格式。



| 名稱       | 類型           | 值                                                             |
|------------|----------------|-------------------------------------------------------------------|
| FormatCode | **REG \_ DWORD** | 16位的正整數，用來識別檔案的格式。 |



 

當使用者嘗試將副檔名為自訂的數位媒體檔案複製到可攜式裝置時，Windows Media Player 會在登錄中尋找與自訂副檔名相關聯的格式代碼。 如果 Windows Media Player 找到格式代碼，則會使用 MTP 來判斷裝置是否支援自訂檔案格式。 如果裝置支援此格式，則會將媒體檔案複製到裝置上，而不會轉碼。

支援 MTP 的裝置可以提供 DeviceInfo 資料集 Windows Media Player，其中包含裝置所支援的格式代碼清單，還有其他專案。

如果您正在開發自訂檔案格式，您可以向 Microsoft 要求格式代碼。 如需有關如何要求格式代碼的詳細資訊，請參閱 microsoft [Windows Media 開發人員中心](https://msdn.microsoft.com/windowsmedia/default.aspx)提供的 Microsoft 媒體傳輸通訊協定移植套件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**副檔名登錄設定**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




