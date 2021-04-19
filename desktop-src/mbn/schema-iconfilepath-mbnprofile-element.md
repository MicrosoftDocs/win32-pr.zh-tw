---
description: 包含連接的圖示檔路徑。
ms.assetid: 9daf4916-914b-4326-9933-b433cc00b4c1
title: ICONFilePath (MBNProfile) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICONFilePath
api_type:
- Schema
ms.openlocfilehash: 6b1e98f76fe2f83ce214076223b5a1439bd0ea45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998458"
---
# <a name="iconfilepath-mbnprofile-element"></a>ICONFilePath (MBNProfile) 元素

**ICONFilePath (MBNProfile)** 元素包含連接的圖示檔路徑。

當使用此專案進行連接時，作業系統連接 UI 會顯示此圖示。

在 [**IMbnConnectionProfileManager**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofilemanager)介面的 [**CreateConnectionProfile**](/windows/desktop/api/mbnapi/nf-mbnapi-imbnconnectionprofilemanager-createconnectionprofile)方法中傳遞用來建立設定檔的 XML 時，此路徑應指向圖示檔的來源位置。 在成功建立 [**IMbnConnectionProfile**](/windows/desktop/api/mbnapi/nn-mbnapi-imbnconnectionprofile) 物件時，行動寬頻服務會複製其內部存放區中的圖示檔，並且會修改設定檔路徑以反映此情況。

圖示檔的格式應為具有32X32 圖元維度的 .bmp 格式。

此元素是長度最多為1024個字元的字串，其中包含絕對檔案路徑。

元素是選擇性的。

``` syntax
<xs:element name="ICONFilePath"
    type="iconFileType"
 />
```

**ICONFilePath** 元素是由 [**MBNProfile**](schema-mbnprofile-element.md)元素定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**MBNProfile**](schema-mbnprofile-element.md)
</dt> </dl>

 

 




