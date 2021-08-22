---
description: 提供 IMFMuxStreamMediaTypeManager 的實例，可用來取得多工媒體來源子串流的媒體類型，以及控制由來源進行多工的子串流的組合。
ms.assetid: 5C36956D-336A-4956-8793-D86DC792E906
title: 'MF_MEDIATYPE_MULTIPLEXED_MANAGER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe00e8824997a0af89099c7fbaad4a2378b44c3360bad0d4b8808023355da2d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973687"
---
# <a name="mf_mediatype_multiplexed_manager-attribute"></a>MF \_ 媒體多工 \_ \_ 管理器屬性

提供 [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager) 的實例，可用來取得多工媒體來源子串流的媒體類型，以及控制由來源進行多工的子串流的組合。

## <a name="data-type"></a>資料類型

**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**

## <a name="remarks"></a>備註

將此值傳遞至 [**IMFAttributes：： GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) ，以取得 [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager)的實例。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1703版桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



 

 
