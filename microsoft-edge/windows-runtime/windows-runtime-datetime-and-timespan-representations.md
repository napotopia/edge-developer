---
title: "Windows Runtime DateTime and TimeSpan Representations | Microsoft Docs"
ms.custom: ""
ms.date: "01/18/2017"
ms.prod: microsoft-edge
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "windows-integration"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "JavaScript, Windows Runtime dates and times"
  - "TimeSpan [JavaScript]"
  - "DateTime [JavaScript]"
ms.assetid: 9743e9ac-9054-463e-8264-427183e4905f
caps.latest.revision: 9
author: "erikadoyle"
ms.author: "edoyle"
manager: "jken"
---
# Windows Runtime DateTime and TimeSpan Representations
The JavaScript representation of dates and times is different from the Windows Runtime version. The Windows Runtime [DateTime](http://msdn.microsoft.com/library/windows/apps/windows.foundation.datetime.aspx) structure is represented in JavaScript as a [Date](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) that has a backing store that matches the `DateTime` data (and has a different range and precision from the JavaScript `Date`). If you modify this custom `Date` object, it becomes a standard JavaScript `Date` and loses precision. JavaScript `Date` values can be passed to a Windows Runtime `DateTime` and will be range-checked, which might result in marshaling exceptions.  
  
 The Windows Runtime [TimeSpan](https://docs.microsoft.com/en-us/uwp/api/windows.foundation.timespan) structure is converted to milliseconds and returned as a JavaScript number.  
  
## See Also  
 [Using the Windows Runtime in JavaScript](./using-the-windows-runtime-in-javascript.md)