---
title: 'IResultVerb 介面 (WdsSharedIDL .h) '
description: 公開動詞屬性。
ms.assetid: 8cc8408e-0117-4344-ad26-0c4a5d09a935
keywords:
- IResultVerb 介面舊版 Windows 環境功能
- IResultVerb 介面舊版 Windows 環境功能，說明
topic_type:
- apiref
api_name:
- IResultVerb
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d922b9e9b3eb93697ed7daf2688001b031db0c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967551"
---
# <a name="iresultverb-interface"></a>IResultVerb 介面

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。 

公開動詞屬性。

## <a name="members"></a>成員

**IResultVerb** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IResultVerb** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IResultVerb** 介面具有這些屬性。



| 屬性                                                             | 存取類型           | Description                                                                                                       |
|:---------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](-search-2x-iresultverb-displayname.md)<br/> | 唯讀<br/>  | 這個屬性會傳回動詞之當地語系化顯示名稱的指標。 <br/>                           |
| [**Doit r**](-search-2x-iresultverb-doit.md)<br/>               | 唯寫<br/> | 執行動詞。 <br/>                                                                                    |
| [**啟用**](-search-2x-iresultverb-enabled.md)<br/>         | 唯讀<br/>  | 如果已啟用動詞，這個屬性會傳回 TRUE。 <br/>                                                    |
| [**HelpText**](-search-2x-iresultverb-helptext.md)<br/>       | 唯讀<br/>  | 這個屬性會傳回動詞的當地語系化說明字串指標。 <br/>                            |
| [**圖示**](-search-2x-iresultverb-icon.md)<br/>               | 唯讀<br/>  | 這個屬性會傳回與動詞相關聯之選擇性圖示的控制碼指標。 <br/>              |
| [**Name**](-search-2x-iresultverb-name.md)<br/>               | 唯讀<br/>  | 這個屬性會傳回動詞的 cononical 名稱指標，例如 print、open 等等。 <br/> |



 

## <a name="remarks"></a>備註

這些方法會公開適用于動詞的屬性和動作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows 桌面搜尋 (WDS) 3。0<br/>                                               |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

