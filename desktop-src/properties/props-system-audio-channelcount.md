---
description: 指出音訊檔案的頻道計數。 Mono 的可能值是1，而針對身歷聲則為2。
ms.assetid: 8a028167-dc0f-4ed9-a710-568caf1b9a47
title: ChannelCount
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9a370e517f8c3552e27bf034c4873b5e1cb593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848681"
---
# <a name="systemaudiochannelcount"></a>ChannelCount

指出音訊檔案的頻道計數。 Mono 的可能值是1，而針對身歷聲則為2。

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10，1703、Windows 10、1607版、Windows 10、1511版、Windows 10、1507、Windows 8.1、Windows 8、Windows 7 版

```
propertyDescription
   name = System.Audio.ChannelCount
   shellPKey = PKEY_Audio_ChannelCount
   formatID = 64440490-4C8B-11D1-8B70-080036B11A03
   propID = 7
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Mono
            value = 1
            text = 1 (mono)
            defineToken = AUDIO_CHANNELCOUNT_MONO
         enum
            name = Stereo
            value = 2
            text = 2 (stereo)
            defineToken = AUDIO_CHANNELCOUNT_STEREO
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.Audio.ChannelCount
   shellPKey = PKEY_Audio_ChannelCount
   formatID = 64440490-4C8B-11D1-8B70-080036B11A03
   propID = 7
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = UInt32
      IsInnate = true
      EnumeratedList
         UseValueForDefault = True
         enum
            value = 1
            text = 1 (mono)
            defineName = AUDIO_CHANNELCOUNT_MONO
         enum
            value = 2
            text = 2 (stereo)
            defineName = AUDIO_CHANNELCOUNT_STEREO
```

## <a name="remarks"></a>備註

PKEY 值定義于 Propkey 中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[>cultureinfo.numberformat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
