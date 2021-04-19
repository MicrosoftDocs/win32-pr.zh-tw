---
description: DirectShow 基類會提供 helper 函式來處理 AM \_ 媒體 \_ 類型結構。
ms.assetid: 4dbea5b4-bf78-4253-be48-d81b77be6e77
title: '媒體類型函數 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Media
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a39fe9a9599a1d85c14a226106f5c8d7080b721f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001490"
---
# <a name="media-type-functions"></a>媒體類型函式

DirectShow 基類會提供 helper 函式來處理 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構。

**AM \_ 媒體 \_ 類型** 結構包含指標 (**pbFormat** 成員) 至另一個記憶體區塊，也就是所謂的 *格式區塊*。 因此，當您使用此結構時，您必須小心處理記憶體配置，以避免記憶體流失。

下列函式會配置記憶體：

-   **CreateMediaType** 會配置新的 **AM \_ 媒體 \_ 類型** 結構和格式區塊。
-   **CopyMediaType** 會複製到現有的 **AM \_ 媒體 \_ 類型** 結構，但會配置格式區塊。
-   **CreateAudioMediaType** 會初始化現有的 **AM \_ 媒體 \_ 類型** 結構，並選擇性地配置格式區塊。

下列功能可用的記憶體：

-   **FreeMediaType** 會釋放格式區塊。
-   **DeleteMediaType** 會釋出 **AM \_ 媒體 \_ 類型** 結構，包括格式區塊。



| 函式                                             | 描述                                                                                                 |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**CopyMediaType**](copymediatype.md)               | 複製工作分配的 **AM \_ 媒體 \_ 類型** 結構。                                                      |
| [**CreateAudioMediaType**](createaudiomediatype.md) | 使用指定的 wave 格式結構，初始化媒體類型結構。                                           |
| [**CreateMediaType**](createmediatype.md)           | 從現有的 **am \_ 媒體 \_ 類型** 結構配置並初始化 **am \_ 媒體 \_ 類型** 結構。 |
| [**DeleteMediaType**](deletemediatype.md)           | 刪除工作配置的 **AM \_ 媒體 \_ 類型** 結構。                                                     |
| [**FreeMediaType**](freemediatype.md)               | 從記憶體釋出工作分配的 **AM \_ 媒體 \_ 類型** 結構。                                           |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Mtype (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




